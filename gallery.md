{% capture newline %}
{% endcapture %}

{% assign image_files = site.static_files | where: "image", true %}

{%- for myimage in image_files -%}
|[![]({{ site.baseurl }}/images/{{ myimage.path }})]({{ site.baseurl }}/images/{{ myimage.path }}){%- cycle "", "", "", newline -%}{%- endfor -%}
