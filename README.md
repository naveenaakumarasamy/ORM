# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![Entity Relationship Diagram](./orm2.png)

## DESIGN STEPS

### STEP 1:
clone the programe from the git hub

### STEP 2:
Create a new app

### STEP 3:
Enter the code for admin.py and models,py

### STEP 4:
Execute Django admin and create 10 employees

Write your own steps

## PROGRAM
```
Model.py


from django.db import models
from django.contrib import admin
class Employee(models.Model):
    eid=models.CharField(max_length = 20,help_text="Employee ID")
    name=models.CharField(max_length = 100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')

Admin.py
from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)
```

## OUTPUT

![OUTPUT](./orm1.png)

## RESULT

Programe executed successfully.