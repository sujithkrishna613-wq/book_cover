# Ex.05 Book Front Cover Page Design
# Date:15-12-2025

# AIM:
To design a book front cover page using HTML and CSS.

# DESIGN STEPS:
## Step 1:
Create a Django Admin project.

## Step 2:
Create an app in the Django interface.

## Step 3:
Create a folder named 'static' in the app folder.

## Step 4:
Create a new HTML file in the static folder.

## Step 5:
Write the HTML code with relevant CSS properties.

## Step 6:
Choose the appropriate style and color scheme.

## Step 7:
Insert the images in their appropriate places.

## Step 8:
Publish the website in the LocalHost.

# PROGRAM:
```
book.html

{% load static %}
<html>
<head>
  <title>Book Cover</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      text-align: center;
    }

    .book-container {
      position: relative;
      display: inline-block;
      margin: 20px;
    }

    .book-cover {
      height: 700px;
      width: 500px;
      display: block;
    }

    .author-image {
      position: absolute;
      bottom: 5px;
      right: 5px;
      width: 80px;
      height: 80px;
      border: 1px solid black;
      box-shadow: 0 0 8px rgba(0,0,0,0.5);
      border-radius: 50px;
    }

    .top{
      position: absolute;
      top: 60px;
      left:10px;
      width: 45%;
      border: 50px;
      border-top: 1px solid #ff6200;
      margin: 10px auto;
    }

    .edition{
      position: absolute;
      top: 35px;
      color: #0022ff;
      font-family: sans-serif;
      font-size: x-large;
      left: 30px;
      margin: 10px auto;

    }
    .bottom{
      position: absolute;
      bottom: 100px;
      width: 50%;
      border: 0;
      border-top: 1px solid #ff4000;
      margin:0 0 10px 300px;
      right: 10PX ;

    }
    .author{
      position: absolute;
      bottom: 4px;
      left: 20px;
      color: #000000;
      font-family: 'Courier New', Courier, monospace;
      font-size: xx-large;
      margin: 10px auto;

    }
    .border{
      position:absolute;
      bottom:10px;
      top:30px;
      right:10px;
      left:10px;
      border:5px solid yellow
    }
    
  </style>
</head>
<body>
  <div class="book-container">
    <div class="border"></div>
    <div class="edition">LIMITED EDITION</div>
    <div class="'middle">FATHER OF INDIAN CONSTITUION</div>
    <hr class="top">
    <hr class="bottom">
    <div class="author">ABINAV | 2023</div>
    <img src="{% static 'bookcover.jpeg' %}" alt="Book Cover" class="book-cover">
    <img src="{% static 'author.jpeg' %}" 
    alt="Author" class="author-image">
</div>


</body>
</html>
```
```
views.py

from django.shortcuts import render

def bookcover(request):
    return render(request, "book.html")
```
```
urls.py

from django.contrib import admin
from django.urls import path
from book import views 

urlpatterns = [
    path('admin/', admin.site.urls),
    path('book/', views.bookcover, name='bookcover')
]
```

# OUTPUT:
![alt text](<Screenshot 2025-12-15 135948.png>)

# RESULT:
The program for designing book front cover page using HTML and CSS is completed successfully.