---
layout: default
---
<style>
/* Rounded and responsive profile image */
.profile-image {
  border-radius: 100%; /* Makes the image rounded */
  max-width: 20%;    /* Ensures the image is responsive and scales with its container */
  height: auto;       /* Automatically adjusts the image's height while maintaining the aspect ratio */
}
/* Apply font styles and make text bold */
.intro h1 {
  font-weight: bold;
}

/* Indent date to the right */
.blog-posts h2 {
  display: flex;
  justify-content: space-between;
  font-size: 1rem; /* Adjust the size as needed */
  color: grey; /* Set the title color to black */
}
/* Indent date to the right */
.blog-posts h2 a{
  display: flex;
  text-decoration: underline;
  justify-content: space-between;
  font-size: 1.1rem; /* Adjust the size as needed */
  color: black; /* Set the title color to black */
}

</style>
<div class="intro">
  <img class="img-responsive profile-image" src="/assets/images/logo.jpg" alt="Your Picture">
  <br><br>
  <h1>Hey, This is Garry Singh</h1>
  <p>
    I'm a passionate technology enthusiast and a dedicated blogger. Here, I share my thoughts on transformative IT solutions, innovation, and more.
  </p>
  <br>
</div>

<div class="blog-posts">
  <ul style="list-style: none; padding-left: 0;margin-left:0;"> <!-- Remove list-style bullets -->
    {% for post in site.posts %}
      <li>
        <!--<img class="img-responsive" src="/assets/images/{{ post.name | remove: '.markdown' }}.jpg" alt="Image Description">-->
        <h2><a href="{{ post.url }}">{{ post.title }}</a> {{ post.date | date: "%b %d, %Y" }}</h2> <!-- Add post date -->
        {{ post.excerpt | strip_html | truncatewords: 50 }} <!-- Shorten excerpt to 20 words -->
      </li>
    {% endfor %}
  </ul>
</div>
