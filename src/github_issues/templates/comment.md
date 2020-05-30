{% if author_name %}From: {% if author_github_username %}{{ author_github_username }} ({{ author_name }}){% else %}**{{ author_name }}**{% endif %}{% endif %}
{% if note_date %}Date: {{ note_date }}{% endif %}

---

{{ description }}

{% if attachments|length > 0 -%}
---
{% for attachment in attachments %}
- [{{ attachment.filename }}]({{ attachment.content_url }}) ({{ attachment.author.name }})
{%- endfor %}
{%- endif %}
