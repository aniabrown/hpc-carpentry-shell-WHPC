---
layout: lesson
carpentry: "swc"
venue: "COM-G12-Main Lewin"
address: "COM-G12-Main Lewin, Computer Science Department, Regent Court, 211 Portobello St, Sheffield"
country: "UK"
language: "English"
latlng: "53.381122, -1.479930"
humandate: "09:00-17:00, 30 Jan 2020, 09:00-16:00 31 Jan 2020"
humantime: "09:00 - 17:00"
startdate: 2020-01-30
enddate: 2020-01-31
instructor: ["Mozhgan Kabiri Chimeh, Anna Brown, Fouzhan Hosseini, Weronika Fillinger, Neelofar Banglawala"]
helper: []
email: [m.kabiri-chimeh@sheffield.ac.uk]
collaborative_notes: https://pad.carpentries.org/2020-01-30-whpc-hpccarpentry
eventbrite: 
root: .
---

{% comment %}
Add sponsor info here
{% endcomment %}

<h2 id="general">General Information</h2>

<p>This workshop is an introduction to using high-performance computing systems effectively. We
obviously can't cover every case or give an exhaustive course on parallel programming in just two
days of teaching time. Instead, this workshop is intended to give students a good introduction and
overview of the tools available and how to use them effectively.</p>

<p>By the end of this workshop, students will know how to:</p>

<ul>
  <li>Know how to connect to remote HPC systems and transfer data</li>
  <li>Know how to use a scheduler to work on a shared system</li>
  <li>Be able to use software modules to access different HPC software</li>
  <li>Be able to work effectively on a remote shared resource</li>
</ul>

<p>The material for the second part of this workshop is available at: <a href="https://aniabrown.github.io/hpc-carpentry-WHPC/">https://aniabrown.github.io/hpc-carpentry-WHPC/</a>.</p>

{% comment %}
Add affiliation info here -- WHPC, our institutions
{% endcomment %}

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
  {% include workshop_calendar.html %}
</p>
{% endif %}

{% comment %}
  SPECIAL REQUIREMENTS

  Modify the block below if there are any special requirements.
{% endcomment %}
<p id="requirements">
  <strong>Requirements:</strong> Participants must bring a laptop with a
  Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.) that they have administrative privileges
  on. They should have a few specific software packages installed (listed
  <a href="#setup">below</a>). They are also required to abide by
  {% if page.carpentry == "swc" %}
  Software Carpentry's
  {% elsif page.carpentry == "dc" %}
  Data Carpentry's
  {% elsif page.carpentry == "lc" %}
  Library Carpentry's
  {% endif %}
  <a href="{{site.swc_site}}/conduct.html">Code of Conduct</a>
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

> ## Prerequisites
> There are no prerequisites for this lesson
{: .prereq}

### Getting Started
<h2 id="setup">Getting Started</h2>

<p>To get started, follow the directions on the <a href="setup/">Setup</a> page to ensure you have the bash shell and an SSH client installed.</p>

<hr/>


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
