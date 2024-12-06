# Ex02 Django ORM Web Application
# Date:25/10/2024
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lamp Power Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            width: 310px;
            text-align: center;
        }
        h1 {
            color: #4CAF50;
            margin-bottom: 20px;
        }
        input[type="number"] {
            width: 95%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        input[type="text"] {
            width: 95%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background: #4CAF50;
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background: #45a049;
        }
        .result {
            margin-top: 20px;
            font-size: 1.2em;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Lamp Power Calculator</h1>
        <form method="post">
            {% csrf_token %}
            <input type="number" name="intensity" step="any" placeholder="Intensity (I)" required>
            <input type="number" name="resistance" step="any" placeholder="Resistance (R)" required>
            <button type="submit">Calculate Power</button>
            <input type="text" id="ans" value="{{power}}" readonly>
        </form>
        {% if result is not None %}
            <div class="result">
                <strong>Power (P):</strong> {{ result }} Watts
            </div>
        {% endif %}
    </div>
</body>
</html>


models.py

from django.db import models
from django.contrib import admin

class Book (models.Model):
  
    book_no=models.IntegerField()
    book_name=models.CharField(max_length=100)
    author_name=models.CharField(max_length=100) 
    Email=models.EmailField()
    buyer_name=models.CharField(max_length=100)
    mobile_no=models.IntegerField()

class BookAdmin(admin.ModelAdmin):
    	list_display= ('book_no', 'book_name', 'author_name', 'Email', 'buyer_name', 'mobile_no')

urls.py

from django.contrib import admin
from django.urls import path

urlpatterns = [
    path('admin/', admin.site.urls),
]

```
# OUTPUT
![orm terminal](https://github.com/user-attachments/assets/038ec4f8-127e-4ab8-a772-4db680b6c45b)
![orm user](https://github.com/user-attachments/assets/5adf124f-a75f-4ab2-ba07-83ce08cd7b9f)
![orm book](https://github.com/user-attachments/assets/dedab270-6faa-4254-b93a-9f072443af00)



# RESULT
Thus the program for creating a database using ORM hass been executed successfully
