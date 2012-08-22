---
layout: post
title: "Center align image with in a div using css"
date: 2012-08-22 11:21
comments: true
categories:
---

### HTML Code

    <div class="container">
      <img src="#" />
    </div>

### CSS Code

    .container {
      position: relative;
    }
    img {
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      margin: auto;
    }
