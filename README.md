# CodePath week 8 - Pentesting Live Targets.

Time spent: **7.5** hours.

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Pentesting Report

## Blue

Vulnerability #1: Session Hijacking/Fixation: You log in to find the Session ID ussing the change_session_id script.
<img src ="blue_1.gif" >
<img src ="blue_2.gif" >
<img src ="blue_3.gif" >
<img src ="blue_4.gif" >

Vulnerability #2: SQL Injection (SQLi): Check the url and find the id, replace the value with "2" . After include sleep(). Ex: " 2' and SLEEP(5)=0--' " 
<img src= "id_1.gif" >
<img src= "id_2.gif" >


## Green

Vulnerability #1: User Enumeration: There is different styling (normal and bold font) for log in errors of valid and invalid usernames.
<img src= "login.gif" >

Vulnerability #2: Cross Site Scripting: Input in the comment box isn't sanitized, so adding a script to a comment allows for an alert box to pop up when a user logs in and clicks on feedback. 
<img src= "contact_1.gif" >
<img src= "contact_2.gif" >


## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR): The ID for each salesman is visible in the URL, by manipulating the numbers, you are able to access 2 salesmen, 1 that had been terminated and 1 that is not supposed to be public until a later date.

<img src= "red1.gif" >

Vulnerability #2: Cross-Site Request Forgery (CSRF): Submitting the url for an html file with malicious code into the feedback page tricks the user into altering data on the salesperson page.

<img src= "red2_1.gif">
<img src= "red2_2.gif">

## Bonus: 
Green- XSS: 
Using scripting in the feedback textbox you can direct the user to a new URL.
<img src= "">
