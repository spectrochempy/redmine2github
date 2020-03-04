{% if author_name %}From: {% if author_github_username %}{{ author_github_username }} ({{ author_name }}){% else %}**{{ author_name }}**{% endif %}{% endif %}
{% if note_date %}Date: {{ note_date }}{% endif %}

---

{{ description }}
