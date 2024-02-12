---
layout: page
permalink: /works/
title: Works
nav: true
nav_order: 16
---

<div class="filter-links">
  <!-- <a href="{{ site.baseurl }}{{ post.url }}/works_2024/">2024</a> |  -->
  <a href="{{ site.baseurl }}{{ post.url }}/works_2023/">2023</a> | 
  <a href="{{ site.baseurl }}{{ post.url }}/works_2022/">2022</a> | 
  <a href="{{ site.baseurl }}{{ post.url }}/works_2020/">2020</a> | 
  <a href="{{ site.baseurl }}{{ post.url }}/works_2019/">2019</a>
</div>

<div class="gallery">
{% for item in site.data.images %}
    {% if item.year == 2023 %}
        <div class="image-container">
            {% include figure.liquid path=item.url class="img-fluid rounded z-depth-1" zoomable=true %}
            <div class="caption">{{ item.caption }} ({{ item.year }})</div>
        </div>
    {% endif %}
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
        width: calc(100% - 20px); /* 이미지 컨테이너의 너비 설정 */
        margin-bottom: 20px;
        position: relative; /* 상대적 위치 설정 */
        cursor: pointer; /* 마우스 커서를 포인터로 변경하여 클릭 가능한 것을 표시 */
    }
    .image {
        width: 100%; /* 이미지를 부모 요소에 맞춰서 크기 조절 */
        height: auto; /* 이미지의 비율 유지 */
    }
    .caption {
        position: absolute; /* 절대 위치 설정 */
        bottom: -60px; /* 이미지 아래로 60px만큼 이동 */
        left: 0; /* 왼쪽으로 정렬 */
        width: 100%; /* 부모 요소의 너비에 맞추기 */
        color: black; /* 텍스트 색상 설정 */
        padding: 10px; /* 내부 여백 설정 */
        box-sizing: border-box; /* 내부 여백이 요소의 크기에 포함되도록 설정 */
    }

    @media only screen and (min-width: 768px) {
        .image-container {
            width: calc(50% - 20px); /* 브라우저 크기가 768px 이상이면 2개의 이미지를 보여줌 */
        }
    }

    @media only screen and (min-width: 1200px) {
        .image-container {
            width: calc(33.33% - 20px); /* 브라우저 크기가 1200px 이상이면 3개의 이미지를 보여줌 */
        }
    }

    .filter-links {
        margin-bottom: 20px;
        text-align: center; /* 필터링 링크를 가운데 정렬합니다. */
    }

    .filter-links a {
        text-decoration: underline;
        cursor: pointer;
        margin: 0 5px; /* 각 링크 사이의 간격을 조정합니다. */
        color: black; /* 링크의 글씨 색상을 검정색으로 설정합니다. */
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
