## Publications

{% assign pubs = site.publications | sort: "yymm" | reverse %}

### Journal Articles
{% for pub in pubs %}
{% if pub.which == "journal" and pub.is_first %}
{% include publication.html pub=pub %}
{% endif %}
{% endfor %}

{% for pub in pubs reversed %}
{% if pub.which == "journal" and pub.is_first == false %}
{% include publication.html pub=pub %}
{% endif %}
{% endfor %}

### Conference Papers
{% for pub in pubs %}
{% if pub.which == "conference" and pub.is_first %}
{% include publication.html pub=pub %}
{% endif %}
{% endfor %}

{% for pub in pubs %}
{% if pub.which == "conference" and pub.is_first == false %}
{% include publication.html pub=pub %}
{% endif %}
{% endfor %}

### Preprints
{% for pub in pubs %}
{% if pub.which == "preprint" and pub.is_first %}
{% include publication.html pub=pub %}
{% endif %}
{% endfor %}

{% for pub in pubs %}
{% if pub.which == "preprint" and pub.is_first == false %}
{% include publication.html pub=pub %}
{% endif %}
{% endfor %}