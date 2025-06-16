---
layout: workshop      # DON'T CHANGE THIS.
carpentry: "dc"    # what kind of Carpentry (must be either "lc" or "dc" or "swc")
venue: "Data Wrangling and Processing for Genomics"
address: "Regeneron, Tarrytown, NY"
country: "us"
language: "en"
latlng: #"41.732190,-72.793431"
humandate: "June 17, 2025"
humantime: "8:30 am - 4:30 pm"
startdate: 2019-06-13
enddate: 2019-06-13
instructor: ["Ayush Shekhar Saxena", "Zebulun Arendsee"]
helper: ["Mohammed Hussain","Aarushi Gajri"]
email: ["ayushshekhar.saxena@regeneron.com"]
collaborative_notes: https://pad.carpentries.org/2025-06-17-genomics-regn
---

{% comment %} See instructions in the comments below for how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
  HEADER

  Edit the values in the block above to be appropriate for your workshop.
  If the value is not 'true', 'false', 'null', or a number, please use
  double quotation marks around the value, unless specified otherwise.
  And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}

{% comment %}
  EVENTBRITE

  This block includes the Eventbrite registration widget if
  'eventbrite' has been set in the header.  You can delete it if you
  are not using Eventbrite, or leave it in, since it will not be
  displayed if the 'eventbrite' field in the header is not set.
{% endcomment %}
{% if page.eventbrite %}
<iframe
  src="https://www.eventbrite.com/tickets-external?eid={{page.eventbrite}}&ref=etckt"
  frameborder="0"
  width="100%"
  height="280px"
  scrolling="auto">
</iframe>
{% endif %}

<h2 id="general">General Information</h2>

{% comment %}
  INTRODUCTION

  Edit the general explanatory paragraph below if you want to change
  the pitch.
{% endcomment %}
{% if page.carpentry == "swc" %}
  {% include sc/intro.html %}
{% elsif page.carpentry == "dc" %}
  {% include dc/intro.html %}
{% elsif page.carpentry == "lc" %}
  {% include lc/intro.html %}
{% endif %}

{% comment %}
  AUDIENCE

  Explain who your audience is.  (In particular, tell readers if the
  workshop is only open to people from a particular institution.
{% endcomment %}
{% if page.carpentry == "swc" %}
  {% include sc/who.html %}
{% elsif page.carpentry == "dc" %}
  {% include dc/who.html %}
{% elsif page.carpentry == "lc" %}
  {% include lc/who.html %}
{% endif %}

{% comment %}
  LOCATION

  This block displays the address and links to maps showing directions
  if the latitude and longitude of the workshop have been set.  You
  can use https://itouchmap.com/latlong.html to find the lat/long of an
  address.
{% endcomment %}
{% if page.latlng %}
<p id="where">
  <strong>Where:</strong>
  {{page.address}}.
  Get directions with
  <a href="//www.openstreetmap.org/?mlat={{page.latlng | replace:',','&mlon='}}&zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q={{page.latlng}}">Google Maps</a>.
</p>
{% endif %}

{% comment %}
  DATE

  This block displays the date and links to Google Calendar.
{% endcomment %}
{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}.
</p>
{% endif %}

{% comment %}
  SPECIAL REQUIREMENTS

  Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
  <strong>Requirements:</strong> Participants must bring a Regeneron laptop
</p>

{% comment %}
  ACCESSIBILITY

  Modify the block below if there are any barriers to accessibility or
  special instructions.
{% endcomment %}
<p id="accessibility">
  <strong>Accessibility:</strong> We are committed to making this workshop
  accessible to everybody.
  The workshop organizers have checked that:
</p>
<ul>
  <li>The room is wheelchair / scooter accessible.</li>
  <li>Accessible restrooms are available.</li>
</ul>
<p>
  Materials will be provided in advance of the workshop and
  large-print handouts are available if needed by notifying the
  organizers in advance.  If we can help making learning easier for
  you (e.g. sign-language interpreters, lactation facilities) please
  get in touch (using contact details below) and we will
  attempt to provide them.
</p>

{% comment %}
  CONTACT EMAIL ADDRESS

  Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
  Please email
  {% if page.email %}
    {% for email in page.email %}
      {% if forloop.last and page.email.size > 1 %}
        or
      {% else %}
        {% unless forloop.first %}
        ,
        {% endunless %}
      {% endif %}
      <a href='mailto:{{email}}'>{{email}}</a>
    {% endfor %}
  {% else %}
    to-be-announced
  {% endif %}
  for more information.
</p>

<hr/>


<h2>Pre-workshop survey</h2>
Please complete <a href="https://www.surveymonkey.com/r/rpythonpreworkshop1">this survey</a> before attending the workshop

<h2>Post-workshop survey</h2>
At the end of the workshop, please fill out the <a href="https://www.surveymonkey.com/r/rpythonpostworkshop">post-workshop survey</a> to let us know how the training was for you and to help us improve future workshops.

<h2>Lessons</h2>
The lessons used in the workshop were developed by <a href="https://datacarpentry.org/">Data Carpentry<a/> under a <a href="https://creativecommons.org/licenses/by/4.0/">Creative Commons</a> license.

<h2 id="schedule">Schedule</h2>
<h3>Room 34-252</h3>

<div class="row">
  <div class="col-md-6">
    <h3>Thursday, June 13</h3>
    <table class="table table-striped">
      <tr> <th>Time</th><th>Subject</th><th>Instructor</th></tr>
      <tr> <td>8:30</td> <td>Setup and Overview</td><td><span></span></td></tr>
      <tr> <td>9:30 - 12:00</td> <td><a href="https://datacarpentry.github.io/shell-genomics/">Introduction to the unix shell for Genomics</a></td><td><span>Zebulun Arendsee</span></td></tr>
      <tr> <td>9:15</td> <td><a href="https://datacarpentry.github.io/wrangling-genomics/">Introduction to genomics</a></td><td><span>Ayush Saxena</span></td></tr>
    </table>
  </div>
</div>

{% comment %}
  Collaborative Notes

  If you want to use an Etherpad, go to

      http://pad.software-carpentry.org/YYYY-MM-DD-site

  where 'YYYY-MM-DD-site' is the identifier for your workshop,
  e.g., '2015-06-10-esu'.
{% endcomment %}
{% if page.collaborative_notes %}
<p id="collaborative_notes">
  We will use this <a href="{{page.collaborative_notes}}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
{% endif %}

<hr/>

<h2 id="syllabus">Syllabus</h2>


<div class="row">
  <div class="col-md-6">
    <h3 id="syllabus-shell">The Unix Shell</h3>
    <ul>
      <li>Files and directories</li>
      <li>History and tab completion</li>
      <li>Pipes and redirection</li>
      <li>Looping over files</li>
      <li>Creating and running shell scripts</li>
      <li>Finding things</li>
      <li><a href="{{site.swc_pages}}/shell-novice/reference">Reference...</a></li>
    </ul>
  </div>
  <div class="col-md-6">
    <h3 id="syllabus-r">Programming in R</h3>
    <ul>
      <li>Working with vectors and data frames</li>
      <li>Reading, transfroming and plotting data</li>
      <li>Creating and using functions</li>
      <li>Loops and conditionals</li>
      <li><a href="{{site.swc_pages}}/r-novice-gapminder/reference">Reference...</a></li>
    </ul>
  </div>
</div>

<hr/>

<h2 id="setup">Setup</h2>
<div id="R"> 
  <ul>
    <li>
      We will teach all sections of this workshop using an <a href="https://bioinfo-dev-trial.regeneron.regn.com">R-studio Server</a>,
      a programming environment that runs in a web browser. 
    </li>
    <li>
      The current versions of the Chrome, Safari and Firefox browsers are all supported
    </li>
    <li>
      To access R-studio, point your browser to <a href="https://bioinfo-dev-trial.regeneron.regn.com">bioinfo-dev-trial.regeneron.regn.com</a> and log in with your Regeneron credentials
    </li>
  </ul>
</div>
