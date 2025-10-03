---
title: Contact
nav:
  order: 5
  tooltip: Email, address, and location
---

# {% include icon.html icon="fa-regular fa-envelope" %}Contact

## Join Us ##

We are actively looking to expand the lab at all levels! The lab is based at Algoma University, a vibrant, new, and rapidly growing research institute located in Brampton. You can learn more about our lab's work on our research and publications pages.

{%
  include button.html
  type="email"
  text="ping.luo@algomau.ca"
  link="ping.luo@algomau.ca"
%}
<!-- {%
  include button.html
  type="phone"
  text="(555) 867-5309"
  link="+1-555-867-5309"
%} -->
{%
  include button.html
  type="address"
  tooltip="Our location on Google Maps for easy navigation"
  link="https://www.google.com/maps/place/Algoma+University/@43.7276109,-79.7506181,12.75z/data=!4m6!3m5!1s0x882b1596f9574643:0xad7612fc9befe7ad!8m2!3d43.6866941!4d-79.7593952!16s%2Fg%2F1tgc0dfs?entry=ttu&g_ep=EgoyMDI1MDgxMy4wIKXMDSoASAFQAw%3D%3D"
%}

{% include section.html %}

{% capture col1 %}

{%
  include figure.html
  image="images/SSM.webp"
  caption="Sault Ste. Marie Campus"
%}

{% endcapture %}

{% capture col2 %}

{%
  include figure.html
  image="images/BRAMPTON.webp"
  caption="Brampton Campus"
%}

{% endcapture %}

{% include cols.html col1=col1 col2=col2 %}

{% include section.html dark=true %}

{% capture col1 %}
24 Queen St. East (A-203)<br>
Brampton, Ontario Canada<br>
L6V 1A3
{% endcapture %}

{% capture col2 %}
1520 Queen Street East<br>
Sault Ste. Marie, Ontario<br>
Canada P6A 2G4
{% endcapture %}

{% capture col3 %}
Tel: 1-888-Algoma-U<br>
(1-888-254-6628)<br>
Info@algomau.ca
{% endcapture %}

{% include cols.html col1=col1 col2=col2 col3=col3 %}
