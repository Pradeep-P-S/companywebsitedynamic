# Dynamic Website Design for a Manufacturing Company
## AIM:
To design a dynamic website for a chip manufacturing company.

## DESIGN STEPS:
### Step 1: 
Requirement collection.
### Step 2:
Creating the layout using HTML and CSS.
### Step 3:
Updating the sample content.
### Step 4:
Choose the appropriate style and color scheme.
### Step 5:
Validate the layout in various browsers.
### Step 6:
Validate the HTML code.
### Step 7:
Create a database model and migrate the database.
### Step 8:
Retrieve data from database and display it in a dynamic webpage.
### Step 9:
Publish the website in the given URL.

## PROGRAM:

### base.html:
```
{% load static %}
<!DOCTYPE html>
<html lang="en">

<head>
    <title>Black Private Limited</title>
    <link rel="stylesheet" href="{% static 'css/layout.css' %}">
    <link rel = "icon" href ="{% static 'img/baseimg.jpg' %}" type = "image/x-icon"> 
              
</head>

<body>
    <div class="container">
    <div class="banner">
        Black Private Limited
    </div>
    <div class="menu">
        <div class="menuitem"><a href="/home">Home</a></div> 
        <div class="menuitem"><a href="/products">Products</a></div>
        <div class="menuitem"><a href="/people">People</a></div> 
        <div class="menuitem"><a href="/contact">Contact</a></div> 
    </div><div class="content">
    {% block content %}    
    {% endblock  %}
    </div>
    <div class="footer">
        Copyright © 2020 Silicon Private Limited, Developed by Pradeep.
    </div>
    </div>
</body>

</html>
```
### contact.html:
```
{% extends "website/base.html" %}

{% block content %}
    <div class="contactuscontent">
        <div class="contactbox">
            <div>
                <img src="/static/img/people1.jpg" alt="contactusimg">
            </div>
        </div>
        <hr/>
        <div class="contactemail"><h1>Email: blackprivatelimited@gmail.com</h1></div>
        <div class="contactphone"><h2>Phone: +91-9159425427</h2></div>
        <div class="contactphone"><h2>Address: © Black pvt,Mountain View, California, United-States</h2></div>
        <hr/>
    </div>

{% endblock %}
```
### home.html:
```
{% extends "website/base.html" %}

{% block content %}
    <div class="homecontent">    
    <h1>About Us</h1>
    <img src="/static/img/buildingimg.jpg" alt="Building">
    <div class="contenttext">
    Silicon Pvt Ltd, provides a broad range of semiconductor and infrastructure software applications that serve the data center, networking, software, broadband, wireless, and storage and industrial markets. Common applications for its products include: data center networking, home connectivity, broadband access, telecommunications equipment, smartphones, base stations, data center servers and storage, factory automation, power generation and alternative energy systems, displays, and mainframe operations and management, and application software development. Some of Silicon's core technologies and products include:
    <ul>
        <li>Memory Chips</li>
        <li>SATA HDD</li>
        <li>SATA SSD </li>
        <li>Broadband Modems</li>
        <li>Wifi Devices</li>
        <li>Switching Devices</li>
        <li>Optical Sensors</li>
    </ul> 
    </div>
    </div>
{% endblock  %}
```
### people.html:
```
{% extends "website/base.html" %}

{% block content %}
<div class="peoplecontent">
    <h1>Our Crew</h1>
    <div class="crewmembers">
        {% for people in peoples %}
        <div class="crewmember">
            <div class="memberimage">
                <img src="{{ people.photo.url }}" alt="member image" height="200" width="250">
            </div>
            <div class="membername">{{ people.Membername }}</div>
            <div class="designation">{{ people.Designation }}</div>
        </div>
        {% endfor %}
    </div>
</div>

{% endblock  %}
```
### product.html:
```
{% extends "website/base.html" %}

{% block content %}
<div class="peoplecontent">
    <h1>Our Crew</h1>
    <div class="crewmembers">
        {% for people in peoples %}
        <div class="crewmember">
            <div class="memberimage">
                <img src="{{ people.photo.url }}" alt="member image" height="200" width="250">
            </div>
            <div class="membername">{{ people.Membername }}</div>
            <div class="designation">{{ people.Designation }}</div>
        </div>
        {% endfor %}
    </div>
</div>

{% endblock  %}
```


## OUTPUT:

![output](static/img/rrr1.jpg)

![output](static/img/rrr2.jpg)

![output](static/img/rrr3.jpg)

![output](static/img/rrr4.jpg)

![output](static/img/ad1.jpg)

![output](static/img/ad2.jpg)

## CODE VALIDATION:

![output](static/img/rrr5.jpg)

![output](static/img/rrr6.jpg)

![output](static/img/rrr7.jpg)

![output](static/img/rrr8.jpg)



## RESULT:

Thus a website is designed for the chip manufacturing company and is hosted in the url http://pradeeep.student.saveetha.in:8000/.
