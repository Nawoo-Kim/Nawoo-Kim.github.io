---
layout: page
permalink: /
nav: false
---

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
        transition: transform 0.3s ease-in-out;
    }
    .expanded {
        transform: scale(1.5); /* 클릭했을 때 이미지 확대 */
        z-index: 1;
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

    @media (max-width: 767px) {
        .gallery {
            gap: 10px; /* 작은 크기의 브라우저에서는 사진 간의 거리를 줄임 */
        }
        .image-container {
            width: calc(33.33% - 10px); /* 작은 크기의 브라우저에서는 이미지 간의 공백 크기만 줄임 */
        }
    }
</style>

<div class="gallery">
{% for item in site.data.mainimages %}
    <div class="image-container">
        <img src="{{ item.url }}" class="image img-fluid rounded z-depth-1" alt="{{ item.alt }}">
        <div class="caption">{{ item.caption }}</div>
    </div>
{% endfor %}
</div>

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
