# Ex02 Django ORM Web Application
## Date: 31-03-24

## AIM
To develop a Django application to store and retrieve data from a Employee database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![Screenshot 2024-03-31 211819](https://github.com/Dhanu654/ORM/assets/148514965/f216b8ee-85c8-42ab-8e79-c43f8bab82ab)



## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 employee

## PROGRAM
~~~
models.py

from django.db import models
from django.contrib import admin
class Employee(models.Model):
    eid=models.CharField(max_length=20,help_text="EmployeeID")
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')

admin.py

from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)

~~~

## OUTPUT
![Screenshot 2024-03-31 201933](https://github.com/Dhanu654/ORM/assets/148514965/e805f237-f634-434e-885a-cee5d6344320)




## RESULT
Thus the program for creating a database using ORM hass been executed successfully
