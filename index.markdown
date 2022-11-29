---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
order: 2
---
# Multimodal learning with graphs 

[In our perspective](https://arxiv.org/abs/2209.03299), we observe that artificial intelligence for graphs (graph AI) has achieved remarkable success in modeling complex systems, ranging from dynamic networks in biology to interacting particle systems in physics. However, the increasingly heterogeneous graph datasets call for multimodal methods that can combine different inductive biases—the set of assumptions that algorithms use to make predictions for inputs they have not encountered during training. Learning on multimodal graph datasets presents fundamental challenges because the inductive biases can vary by data modality and graphs might not be explicitly given in the input. 

To address these challenges, multimodal graph AI methods combine different modalities while leveraging cross-modal dependencies. [Here, we survey 145 studies](https://arxiv.org/abs/2209.03299) in graph AI and realize that diverse datasets are increasingly combined using graphs and fed into sophisticated multimodal methods, specified as image-intensive, knowledge-grounded and language-intensive models. Using this categorization, we introduce a blueprint for multimodal graph AI to study existing methods and guide the design of future methods.

![align="center"](images/Figure1.jpg)
*Shown on the left are the different data modalities covered in our [multimodal graph learning perspective](https://arxiv.org/abs/2209.03299). Shown on the right are key machine learning tasks for which multimodal graph learning (MGL) has been used successfully.*

Below are studies from our [perspective](https://arxiv.org/abs/2209.03299) and the community on multimodal graph learning (MGL) and how they fall under the MGL blueprint. This website is meant as (1) a resouorce to those looking to use MGL for their application but unsure how each compoonent is realized in practice and (2) a map of MGL as an emerging field.

**This table is live meaning anyone can submit a study to be considered for this table** and we will update the table **every week**. Entries are grouped by application area. 

## Use this [link](https://forms.gle/ACBwCCfH6UzTeaBZ8) to submit a study to be added to this table.

<br />

<table id = "mgl" class="display">
  {% for row in site.data.mgl %}
      {% if forloop.first %}
        <thead>
        <tr>
          {% for pair in row %}
            <th>{{ pair[0] }}</th>
          {% endfor %}
        </tr>
        </thead>
      {% endif %}
    
        {% tablerow pair in row %}
      		{% if pair[0] == "Method" %}
      			{% assign beatles = pair[1] | split: "-" %}
      		  <a href = "{{ beatles[1] }}"> {{ beatles[0] }} </a> 
      		{% else %}
      		   {{ pair[1] }}
      		{% endif %}
          {% endtablerow %}
      
    {% endfor %}
</table>


<script type="text/javascript" class="init">
$(document).ready(function() {
  // Create a new DataTable object
  table = $('#mgl').DataTable();
});
</script>

  

<br />
<br />




