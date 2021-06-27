---
layout: page
permalink: /publications/index.html
title: Publications
pubs:
  - author: "Linfeng Zhang}, Jiebo Song, Anni Gao, Jingwei Chen, Chenglong Bao, Kaisheng Ma"
    title: "Be Your Own Teacher: Improve the Performance of Convolutional Neural Networks via Self Distillation"
    year: "2019"
    booktitle: "IEEE International Conference on Computer Vision (2019)"

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


