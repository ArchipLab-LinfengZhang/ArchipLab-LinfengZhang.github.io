---
layout: page
permalink: /publications/index.html
title: Publications
pubs:


  - author: "Linfeng Zhang, Chenglong Bao, Kaisheng Ma"
    title: "Self-Distillation: Towards Efficient and Compact Neural Networks"
    month: "March"
    year: "2021"
    booktitle: "IEEE Transactions on Pattern Analysis and Machine Intelligence"
    url: "https://ieeexplore.ieee.org/abstract/document/9381661"

  - author: "Jason Ansel, Han Hong, Jessie Li"
    title: "OLS and 2SLS in Randomized and Conditionally Randomized Experiments"
    month: "March"
    year: "2018"
    booktitle: "Journal of Economics and Statistics"
    url: "https://doi.org/10.1515/jbnst-2018-0016"


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




