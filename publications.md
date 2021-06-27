---
layout: page
permalink: /publications/index.html
title: Publications
pubs:
  - author: "Jason Ansel, Marek Olszewski"
    title: "BFTree - Scaling HotStuff to Millions of Validators"
    month: "June"
    year: "2019"
    booktitle: "Whitepaper"
    url: "https://medium.com/celohq/bftree-scaling-hotstuff-to-millions-of-validators-7d6930ee046a"

  - author: "Dongqi Su, Ying Yin Ting, Jason Ansel"
    title: "Tight Prediction Intervals Using Expanded Interval Minimization"
    month: "June"
    year: "2018"
    booktitle: "Technical Report"
    url: "https://arxiv.org/abs/1806.11222"


---

# Publications

{% for pub in page.pubs %}
{% unless pub.hidden %}
  - {% if pub.url %} [{{pub.title}}]({{pub.url}}).
    {% else %} {{pub.title}}.
    {% endif %}{% if pub.type %}({{pub.type}})
    {% endif %}<br>
    {{pub.author}}.<br>
    {% if pub.type == 'Technical Report' %}{{pub.number}}
    {% endif %}{{pub.booktitle}}{{pub.school}}{{pub.journal}}.<br>
    {% if pub.address %}{{pub.address}}.
    {% endif %} {{pub.month}}, {{pub.year}}. {% if pub.slides %}[Slides]({{pub.slides}}).
    {% endif %}{% if pub.key %}[Bibtex](http://groups.csail.mit.edu/commit/bibtex.cgi?key={{pub.key}}).
    {% endif %}{% if pub.bibtex %}[Bibtex]({{pub.bibtex}}).
    {% endif %}
{% endunless %}
{% endfor %}


