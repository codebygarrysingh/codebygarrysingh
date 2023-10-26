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
.button {
    display: inline-block;
    padding: 10px 20px;
    background-color: #0056b3;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    margin-right: 10px;
    transition: background-color 0.3s; /* Add transition for smooth color change */
  }

  .button:hover {
    background-color: #007bff; /* Change color on hover */
  }

  .icon {
    margin-right: 10px;
    color: #fff; /* Set the icon color to white */
  }
  .blog-posts li{
	margin-bottom: 20px;
  }
</style>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
<div class="intro">
  <img class="img-responsive profile-image" src="/assets/images/logo.jpg" alt="Your Picture">
  <br><br>
  <h1>Hey, This is Garry Singh</h1>
  <p>
    I'm a passionate technology enthusiast and a dedicated blogger. Here, I share my thoughts on transformative IT solutions, innovation, and more.
  </p>
</div>
<div>
    <a href="/about"> <!-- Updated the link to point to the About page -->
      <button class="button">
        <i class="fas fa-cogs icon"></i> <!-- Icon for "What I bring to the table" -->
        What I bring to the table
      </button>
    </a>
    <a href="https://www.linkedin.com/in/singhgarry/">
      <button class="button">
        <i class="fab fa-linkedin-in icon"></i> <!-- Icon for "Connect with Garry" -->
        Connect with Garry
      </button>
    </a>
	<a href="mailto:garry.singh@intelsoft.ca?subject=Hiring%20Inquiry:%20Garry%20Singh%20Blog">
      <button class="button">
        <i class="fas fa-envelope icon"></i> <!-- Icon for "Hire Garry" -->
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
