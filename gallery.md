{% capture newline %}
{% endcapture %}

{% assign image_files = site.static_files | where: "image", true %}

{%- for myimage in image_files -%}
|[![]({{ site.baseurl }}{{ myimage.path }})]({{ site.baseurl }}{{ myimage.path }}){%- cycle "", "", "", newline -%}{%- endfor -%}
