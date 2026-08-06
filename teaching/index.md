---
title: Teaching
nav:
  order: 4
  tooltip: Courses taught by Ping Luo
---

# {% include icon.html icon="fa-solid fa-graduation-cap" %}Teaching

Courses taught by Ping Luo.

<!--
To revise a course illustration later, replace its file in images/teaching while
keeping the same filename, or update the image path in the matching block below.
-->

{% capture introduction_to_computer_science %}

An introduction to programming, problem-solving, algorithms, and computational
thinking. Students develop the foundational skills needed to design and reason
about computer programs.

{% endcapture %}

{%
  include feature.html
  image="images/teaching/introduction-to-computer-science.webp"
  title="COSC 1046 — Introduction to Computer Science"
  text=introduction_to_computer_science
%}

{% capture data_structures %}

An exploration of how data can be organized and accessed efficiently using
arrays, linked structures, stacks, queues, trees, and graphs, with attention to
the trade-offs behind each approach.

{% endcapture %}

{%
  include feature.html
  image="images/teaching/data-structures.webp"
  title="COSC 2006 — Data Structures"
  text=data_structures
  flip=true
%}

{% capture data_analysis_with_python %}

A practical introduction to preparing, exploring, analyzing, and visualizing
data with Python. Students learn to turn raw datasets into clear, evidence-based
insights.

{% endcapture %}

{%
  include feature.html
  image="images/teaching/data-analysis-with-python.webp"
  title="COSC 5806 — Data Analysis with Python"
  text=data_analysis_with_python
%}

{% capture bioinformatics %}

An introduction to computational methods for biological data, including
sequence analysis, genomics, and the interpretation of complex molecular
datasets.

{% endcapture %}

{%
  include feature.html
  image="images/teaching/bioinformatics.webp"
  title="BIOL/COSC XXXX — Bioinformatics"
  text=bioinformatics
  flip=true
%}

{% capture computer_graphics %}

An introduction to the principles behind two- and three-dimensional graphics,
including geometric transformations, modeling, rendering, lighting, and visual
computing.

{% endcapture %}

{%
  include feature.html
  image="images/teaching/computer-graphics.webp"
  title="COSC 3306 — Computer Graphics"
  text=computer_graphics
%}
