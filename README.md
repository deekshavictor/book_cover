# Ex.05 Book Front Cover Page Design
# Date:05/12/2025
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
views.py

from django.shortcuts import render
def book_cover(request):
    return render(request,'book.html')

```
```
urls.py

from django.contrib import admin
from django.urls import path
from bookapp import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.book_cover),
]

```
```
book.html

{%load static%}
<html>
<head>


  <title>Book Cover</title>
  <style>

    .book-cover {
      
      background:url"{%static 'cover.jpg'%}";
      margin:0;
      text-align: center;
      position:relative;
      padding: 20px;
      background-size: 100% 100%;
      height: 80%;
      width: 25%;
      margin-left: 35%;
    }

   

    .author {
      position: absolute;
      bottom: 30px;
      right: 50%;
     
    }
    .author img{
      width: 50px;
      height: 50px;
      border-radius: 1%;
      border: #040404;
      margin-top:30px;
      
    }
    h1{
    font-family: 'Cinzel', serif;
    font-size: 48px;
    font-weight: 600;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: #fffefe;
    text-align: center;
    line-height: 1.25;

    }
    h4{
       font-style: italic;
       font-family: 'Times New Roman', Times, serif;
       font-size: 16px;
       color: rgb(255, 111, 1);
       letter-spacing: 1px;

    }
    .two{
       position: absolute;
       border:2px solid black;
       height:95%;
       width:95%;
       left: 2.1%;
       bottom: 2.5%;
    }
    .author p{
      margin-top: 10px;
      font-size: 16px;
      font-weight: bold;
      color: rgb(247, 246, 244);
    }
    .hr{
      position: absolute;
      bottom:5%;
      border:1px solid black;
      width:50%;
      
    }
    
  </style>
</head>
<body>

  <div class="book-cover">
    <div class="two"></div>
    <h1>Echoes <br>Beneath <br>the <br>Moon</h1>
    <hr>
    <h4>On the edge of silence, horizons whisper secrets untold.</h4>
    <hr>
    <div class="author">
      <img src= "{%static 'author.jpeg'%}" alt="Author">
      <p>DEEKSHA VICTOR</p>
    </div>
  </div>

</body>
</html>

```

# OUTPUT:
![alt text](<Screenshot 2025-12-15 220011.png>)
# RESULT:
The program for designing book front cover page using HTML and CSS is completed successfully.
