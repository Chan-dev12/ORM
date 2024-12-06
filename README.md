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
