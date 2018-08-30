---
#
# See the Github wiki for how to use Markdown in the editable content below:
# link here
#
# Title and Description display on the page and in HTML meta tags
#
title: Resources
description: Guidance, tips, and examples of specific activities you can use throughout the Digital Delivery lifecycle.
#
# Editable - list of guides to include on this page
# Don't need to edit anything but the "guides" section below
#
guides:
  - title: User research guide
    description: Information and guidance for conducting research for the Veteran Tools Platform.
    linkto: user-research
  - title: Design guide
    description: Understand the Veteran Tools Platform design patterns and design guidelines, and download the design tools.
    linkto: design
  - title: Content guide
    description: Review the content style guide for the Veteran Tools Platform.
    linkto: https://github.com/department-of-veterans-affairs/vets.gov-content-style-guide
    target: yes
  - title: Technical guide
    description: Get access to developer tools and learn how to use them.
    linkto: technical
  - title: Agile guide
    description: Manage your team's agile workflow while working on the Veteran Tools Platform.
    linkto: agile
  - title: More resources
    description: A collection of additional resources referred to throughout the <i>Digital Delivery Guide</i>.
    linkto: more
#
# Don't edit items below - they control the page layout
#
return-top: yes
layout: page
page-type: page
page-description: yes
sidebar-page-type: /resources
permalink: /resources/index.html
header-image: /assets/img/image-resources.png
header-image-alt: Resources icon
#
---

<div class="list-files resources-index">

  <ul>

{% for resource in page.guides %}

    <li>

      <a title="{{resource.title}}"
      href="
      {% if resource.target == true %}
      {{resource.linkto}}
      {% else %}
      {{site.baseurl}}/resources/{{resource.linkto}}
      {% endif %}
      "{% if resource.target == true %} target="_blank"{% endif %}>{{resource.title}}</a>

      <ul>

        <li>

          {{resource.description}}

        </li>

      </ul>

    </li>

{% endfor %}

  </ul>

</div>