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

  - author: "Xiaolong Ma, Shen Lin, Shaokai Ye, Zhezhi He, Linfeng Zhang, Geng Yuan, Sia Huat Tan, Zhenggang Li, Deliang Fan, Xuehai Qian, Xue Lin, Kaisheng Ma, Yanzhi Wang"
    title: "Non-Structured DNN Weight Pruning--Is It Beneficial in Any Platform?"
    month: "March"
    year: "2021"
    booktitle: "IEEE Transactions on Neural Networks and Learning Systems"
    url: "https://arxiv.org/pdf/1907.02124.pdf"

  - author: "Linfeng Zhang, Kaisheng Ma"
    title: "Improve Object Detection with Feature-based Knowledge Distillation: Towards Accurate and Efficient Detectors"
    year: "2021"
    booktitle: "The Ninth International Conference on Learning Representations(ICLR2021)"
    url: "https://openreview.net/pdf?id=uKhGRvM8QNH"
    
      - author: "Yuni Lai, Linfeng Zhang, Donghong Han, Rui Zhou, Guoren Wang"
    title: "Fine-grained emotion classification of Chinese microblogs based on graph convolution networks"
    month: "September"
    year: "2020"
    booktitle: "Springer US"
    url: "https://arxiv.org/pdf/1912.02545.pdf"
    
  - author: "Linfeng Zhang, Yukang Shi, Zuoqiang Shi, Kaisheng Ma, Chenglong Bao"
    title: "Task-Oriented Feature Distillation"
    year: "2020"
    booktitle: "Advances in Neural Information Processing Systems"
    url: "https://proceedings.neurips.cc/paper/2020/file/a96b65a721e561e1e3de768ac819ffbb-Paper.pdf"
    
   - author: "Linfeng Zhang, Muzhou Yu, Tong Chen, Zuoqiang Shi, Chenglong Bao, Kaisheng Ma"
    title: "Auxiliary training: Towards accurate and robust models"
    year: "2020"
    booktitle: "Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition"
    url: "https://openaccess.thecvf.com/content_CVPR_2020/papers/Zhang_Auxiliary_Training_Towards_Accurate_and_Robust_Models_CVPR_2020_paper.pdf" 
    

    
    
    
    


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




