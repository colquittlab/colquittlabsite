---
title: Home
---


{% include section.html %}

{% capture col1 %}
   {%
    include figure.html
    image="images/song-system.png"
   %}
{% endcapture %}

{% capture col2 %}
   {%
    include figure.html
    image="images/song_learning_schematic.png"
   %}
{% endcapture %}

{% capture col3 %}
   {%
    include figure.html
    image="images/science_all_cells_umap.png"
   %}
{% endcapture %}



{%
  include cols.html
  col1=col1
  col2=col2
  col3=col3
%}

{% include section.html %}

#### To understand the development and evolution of behavioral complexity, we study the mechanisms that drive the diversification of neurons and neural circuits in birds.
{:.center}
#### We focus on the neural circuitry that is dedicated to the production and learning of birdsong, a spectacularly complex behavior that is a powerful model for understanding the neural mechanisms of sensorimotor development.
{:.center}

{% include section.html %}

{% capture text %}
Our lab combines advanced molecular techniques, bioinformatics, imaging, and behavioral analysis to understand:
- the gene regulatory networks that build birdsong neural circuitry during development
- how these networks intersect with experience during birdsong learning
- how modifications to these networks contributed to the evolution of birdsong and other complex learned behaviors.

{%
  include link.html
  link="research"
  text="See what we're working on"
  icon="fas fa-arrow-right"
  flip=true
%}
{:.center}

{% endcapture %}

{%
  include feature.html
  image="images/banner_image_96dpi.png"
  link="research"
  title="Our Research"
  text=text
%}


{% capture text %}

The Colquitt Lab opened in August of 2022, and we’re excited to build a team of stellar researchers.

{%
  include link.html
  link="team"
  text="Meet our team"
  icon="fas fa-arrow-right"
  flip=true
%}
{:.center}

{% endcapture %}

{%
  include feature.html
  image="images/BF_pic.png"
  link="team"
  title="Our Team"
  text=text
%}
