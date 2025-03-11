---
layout: page
title: Volunteer Matcher Webapp
description: Software Design, Fall 2024
img: assets/img/volunteerMatcher/homepage.png
importance: 2
category: 2024
---

Source code:
[Github Repository](https://github.com/cindyddang/VolunteerMatcher) 

This repository is forked from the main branch of my friend's [repository](https://github.com/Ryan-Gunawan/COSC-4353) where we worked together throughout the Fall 2024 semester to create this wonderful webpage.

The Volunteer Matcher Web Application is designed to connect volunteers with organizations that need assistance. The platform allows organizations to post volunteer opportunities, and volunteers can browse and sign up for roles that match their skills and interests. 

First, the website will have a login/register page where it will assign each login a cookie session. There will be 2 types of accounts: admin and volunteer. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/volunteerMatcher/login.png" %}
    </div>
</div>
<div class="caption">
    Login/Register page
</div>

Admin will be allowed to create an event, while volunteer will be a user who searches for event. Each new user will be prompt to fill a profile form before allowed to proceed to home page.


<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/volunteerMatcher/profile.png" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/volunteerMatcher/history.png" %}
    </div>
</div>
<div class="caption">
    Profile page and User History page
</div>

After that, users are all set. They can start exploring events. And for every matched events, it will be stored in user's database and displayed in their history.

At the end of every event, admins will be able to rate a volunteer's performance. They can also export the report as PDF or CSV files. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/volunteerMatcher/csv_report.png" %}
    </div>
</div>
<div class="caption">
    An example of CSV report
</div>

Additional features: admins are able to edit any created event, sends notifications to users when a new event-volunteer is matched,...