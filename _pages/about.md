---
layout: page
title: about
permalink: /aboutnotuse/
nav: false
# subtitle: <a href='#'>예원</a>. Address. now__kim_. Moto. Etc.

# profile:
#   align: right
#   image: nwkim_profile.jpeg
#   image_circular: false # crops the image to make it circular
#   # more_info: >
#   #   <p>555 your office number</p>
#   #   <p>123 your address street</p>
#   #   <p>Your City, State 12345</p>

# news: false # includes a list of news items
# latest_posts: false # includes a list of the newest posts
# selected_papers: false # includes a list of papers marked as "selected={true}"
# social: false # includes social icons at the bottom of the page
---

<div class="gallery">
{% for item in site.data.mainimages %}
    <div class="image-container">
        {% include figure.liquid path=item.url class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>    
{% endfor %}
</div>

<style>
    .gallery {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        gap: 20px;
        margin-bottom: 20px;
    }
    .image-container {
        width: calc(33.33% - 20px); /* 항상 3개의 이미지를 보여주기 위해 너비 조정 */
        margin-bottom: 20px;
        position: relative;
        cursor: pointer;
    }
    .image {
        width: 100%;
        height: auto;
    }
    .caption {
        position: absolute;
        bottom: -60px;
        left: 0;
        width: 100%;
        color: black;
        padding: 10px;
        box-sizing: border-box;
    }
</style>

<script>
document.addEventListener("DOMContentLoaded", function(event) {
  const images = document.querySelectorAll('.image');

  images.forEach(image => {
    image.addEventListener('click', () => {
      // 이미지를 클릭했을 때 확대되도록 설정
      if (image.classList.contains('expanded')) {
        image.classList.remove('expanded');
      } else {
        image.classList.add('expanded');
      }
    });
  });
});
</script>
