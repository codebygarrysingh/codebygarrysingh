---
layout: default
---

<head>
  <!-- Other head elements -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
    <link rel="stylesheet" type="text/css" href="{{ '/assets/style/main.css' | relative_url }}">
</head>

<body>
<div class="intro">
  <div class="text">
    <p class="academics-summary">
      I am currently pursuing a <a href="https://www.ox.ac.uk/admissions/graduate/courses/msc-software-engineering" target="_blank">MSC in Computer Engineering</a> at the University of Oxford, UK. My academic journey began with a <a href="https://www.sheridancollege.ca/en/about/faculties/applied-science-technology" target="_blank">B.Eng. in Computer Engineering</a> from Sheridan Institute of Technology in Canada, complemented by a <a href="https://www.vmsuniversity.in/course/bachelor-of-business-administration-bba/">Bachelor's in Business Administration</a> from Vinayaka Missions Sikkim University in India.
	</p>
<p class="work-summary">
With a background spanning over a decade, I have served in pivotal roles as a Software Engineering Lead, Senior Data Engineer & Enterprise Data Integration Consultant with major North American banks including <a href="https://www.rbccm.com/en/gib/technology.page" target="_blank">Royal Bank of Canada</a> & <a href="https://jobs.td.com/en-CA/job-opportunities/corporate/information-technology/" target="_blank">Toronto Dominion Bank</a>, renowned retail giant <a href="https://www.albertsons.com/">Albertsons</a>, <a href="https://www.canada.ca/en/employment-social-development/programs/benefits-delivery-modernization.html" target="_blank">Government of Canada</a> and <a href="https://www.ibm.com/ca-en" target="_blank">IBM</a>.
</p>
<p class="entrepreneurship-summary">
I've also ventured into entrepreneurship, founding <a href="https://intelsoft.ca/" target="_blank">IntelSoft</a>, a company specializing in big data and business intelligence solutions. </p>
<p class="learning-summary">
I am a <a href="https://learn.microsoft.com/api/credentials/share/en-us/GurpartapSingh-5490/69A18CDE02E48F54?sharingId=A4A35DC5E5B5F9F6" target="_blank">certified Microsoft Applied AI Engineering Practitioner on Azure Cloud</a> and have completed <a href="https://www.coursera.org/account/accomplishments/certificate/" target="_blank">specializations in Machine Learning</a> and <a href="https://coursera.org/share/667eb8e180ea744cc543269a96794b6e" target="_blank">Mathematics for Machine Learning and Data Science</a> from Stanford University and Deep Learning AI.
</p>

  </div>
	  <img class="profile-image" src="/assets/images/logo.jpg" alt="Your Picture">
	  
</div>
<br>

<div class="blog-posts">
  <!-- Latest Publications -->
  <h1 class="publications-title">Latest Publications</h1>

  <br>
  <ul> <!-- Remove list-style bullets -->
    {% for post in site.posts %}
      <li>
	  	<hr>
        <!--<img class="img-responsive" src="/assets/images/{{ post.name | remove: '.markdown' }}.jpg" alt="Image Description">-->
        <h2><a href="{{ post.url }}">{{ post.title }}</a> <span class="post-date">{{ post.date | date: "%b %d, 2023" }}</span></h2> <!-- Add post date -->
		<h2><span class="post-date-mob">{{ post.date | date: "%b %d, 2023" }}</span></h2>
        {{ post.excerpt | strip_html | replace: "In the Brief", "" | truncatewords: 50 }}
      </li>
    {% endfor %}
  </ul>
  
  <!-- Upcoming Publications -->
  <h1 class="publications-title">Upcoming Publications</h1>
  <br>
  <ul class="upcoming-publications-list">
    <li>	<hr>Supervised Learning: All you need to know to get started<span class="coming-soon-tag">Coming Soon</span></li>
  </ul>
</div>
</body>