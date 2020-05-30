{% if author_name %}Author: {% if author_github_username %}{{ author_github_username }} ({{ author_name }}){% else %}**{{ author_name }}**{% endif %}{% endif %}
{% if start_date %}Date: {{ start_date }}{% endif %}
{% if redmine_link %}Redmine Issue: {{ redmine_issue_num }}, {{redmine_link}}{% endif %}

---

{{ description }}

{% if attachments|length > 0 -%}
---
{% for attachment in attachments %}
- [{{ attachment.filename }}]({{ attachment.content_url }}) ({{ attachment.author.name }})
{%- endfor %}
{%- endif %}
