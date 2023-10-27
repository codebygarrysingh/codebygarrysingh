---
layout: default
---
<head>
  <!-- Other head elements -->

  <link rel="stylesheet" type="text/css" href="{{ '/assets/style/main.css' | relative_url }}">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
</head>

<div class="intro">
  <img class="img-responsive profile-image" src="/assets/images/logo.jpg" alt="Your Picture">
  <br><br>
  <h1>Hey, This is Garry Singh</h1>
  <p>
    I'm a passionate technology enthusiast and a dedicated blogger. Here, I share my thoughts on transformative IT solutions, innovation, and more.
  </p>
</div>
<div>
    <a href="/about">
      <button class="button">
        <i class="fas fa-cogs icon"></i> 
        What I bring to the table
      </button>
    </a>
    <a href="https://www.linkedin.com/in/singhgarry/">
      <button class="button">
        <i class="fab fa-linkedin-in icon"></i> 
        Connect with Garry
      </button>
    </a>
	<a href="mailto:garry.singh@intelsoft.ca?subject=Hiring%20Inquiry:%20Garry%20Singh%20Blog">
      <button class="button">
        <i class="fas fa-envelope icon"></i>
        Hire Garry
      </button>
    </a>
  </div>
  
  <br><br>

<div class="blog-posts">
  <ul style="list-style: none; padding-left: 0;margin-left:0;"> <!-- Remove list-style bullets -->
    {% for post in site.posts %}
      <li>
        <!--<img class="img-responsive" src="/assets/images/{{ post.name | remove: '.markdown' }}.jpg" alt="Image Description">-->
        <h2><a href="{{ post.url }}">{{ post.title }}</a> {{ post.date | date: "%b %d, 2023" }}</h2> <!-- Add post date -->
        {{ post.excerpt | strip_html | truncatewords: 50 }} <!-- Shorten excerpt to 20 words -->
      </li>
    {% endfor %}
  </ul>
</div>
