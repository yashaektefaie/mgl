---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
# Overview

This website hosts a table to highlight selected studies from the perspective on [multimodal graph learning (MGL)](https://arxiv.org/abs/2209.03299) and the community in a supplementary table and how they fall under the MGL blueprint. **This table is live meaning anyone can submit a study to be considered for this table** and we will update the table **every week**. Entries are grouped by application area. This table is meant as (1) a resouorce to those looking to use MGL for their application but unsure how each compoonent is realized in practice and (2) a map of MGL as an emerging field.

# Multimodal Graph Learning Refresher

### *From the [MGL perspective](https://arxiv.org/abs/2209.03299) abstract:*

Artificial intelligence on graphs (graph AI) has achieved remarkable success in modeling complex systems, ranging from dynamical systems in biology to interacting particle systems in physics. The increasingly hetero- geneous graph datasets call for multimodal graph AI algorithms to combine multiple inductive biases—the set of assumptions that algorithms use to predict outputs of given inputs that they have not yet encountered. Learning on multimodal graph datasets presents fundamental challenges because inductive biases can vary by data modality and graphs might not be explicitly given in the input. To address these challenges, multimodal graph AI methods combine multiple modalities while leveraging cross-modal dependencies. Here, we survey 142 studies in graph AI and realize that diverse datasets are increasingly combined using graphs and fed into sophisticated multimodal models. These models stratify into image-, language-, and knowledge-grounded multimodal graph AI methods. Using this categorization of state-of-the-art methods, we put forward an algorithmic blueprint for multimodal graph AI, which we use to study existing methods and standardize the design of future methods for highly complex systems.

### *From the [MGL perspective](https://arxiv.org/abs/2209.03299) Figure 1:*

![align="center"](images/Figure1.jpg)
*Shown on the left are the different data modalities covered in our multimodal graph learning perspective. Shown on the right are key machine learning tasks for which multimodal graph learning has been used successfully. This Perspective introduces the multimodal graph learning (MGL) blueprint that serves as a unifying framework within which multimodal graph neural architectures can be expressed. It also surveys applications of MGL in computer vision, natural language processing, and natural sciences. This website displays these studies in a supplementary table and how they fall under the MGL blueprint.*

For more information please read our perspective [here](https://arxiv.org/abs/2209.03299).


# Table

<table>
  {% for row in site.data.mgl %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
		{% if pair[0] == "Method Name" %}
			{% assign beatles = pair[1] | split: "-" %}
		    <a href = "{{ beatles[1] }}"> {{ beatles[0] }} </a>
		{% else %}
		    {{ pair[1] }}
		{% endif %}
    {% endtablerow %}
  {% endfor %}
</table>

## Use this [link](https://forms.gle/ACBwCCfH6UzTeaBZ8) to submit a study to be added to this table.


