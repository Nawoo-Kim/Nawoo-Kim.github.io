---
layout: page
permalink: /teaching/
title: teaching
description: Materials for courses you taught. Replace this text with your description.
nav: false
nav_order: 6



# profiles:
#   - image: image1.jpg
#     more_info: "Additional info for image 1"
#     content: "content_for_image1.md"
#   - image: image2.jpg
#     more_info: "Additional info for image 2"
#     content: "content_for_image2.md"
#   - image: image3.jpg
#     more_info: "Additional info for image 3"
#     content: "content_for_image3.md"

---

<!-- gallery.html -->
<div class="row">
{% for item in site.data.gallery %}
    <div class="image">
        <img src="{{ item.image }}" alt="{{ item.alt }}">
        <div class="caption">{{ item.caption }}</div>
    </div>
{% endfor %}
</div>

<style>
    .row {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
    }
    .image {
        width: calc(33.33% - 20px); /* 3개의 이미지를 균등하게 배치하되 간격을 조절 */
        margin-bottom: 20px;
        position: relative; /* 상대적 위치 설정 */
    }
    .image img {
        width: 100%; /* 이미지를 부모 요소에 맞춰서 크기 조절 */
        height: auto; /* 이미지의 비율 유지 */
    }
    .caption {
        position: absolute; /* 절대 위치 설정 */
        bottom: 0; /* 아래쪽으로 정렬 */
        left: 0; /* 왼쪽으로 정렬 */
        width: 100%; /* 부모 요소의 너비에 맞추기 */
        background-color: rgba(0, 0, 0, 0.5); /* 배경색 및 투명도 설정 */
        color: #fff; /* 텍스트 색상 설정 */
        padding: 10px; /* 내부 여백 설정 */
        box-sizing: border-box; /* 내부 여백이 요소의 크기에 포함되도록 설정 */
    }
</style>



<!-- ## 10

For now, this page is assumed to be a static description of your courses. You can convert it to a collection similar to `_projects/` so that you can have a dedicated page for each course.

Organize your courses by years, topics, or universities, however you like! -->