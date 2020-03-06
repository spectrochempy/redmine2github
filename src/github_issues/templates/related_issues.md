{{ original_description }}

{% if  related_issues or child_issues_github %}

---

{% if related_issues %}Related issue(s): {{ related_issues }}{% endif %}
{% if child_issues_github %}Child issue(s): {{ child_issues_github }}{% endif %}

{% endif %}
