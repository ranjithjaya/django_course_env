# [Python Django Course for Beginners 2021](https://www.youtube.com/watch?v=t7DrJqcUviA)
[CSS files used in this tutorial:](https://github.com/academind/django-practical-guide-course-code/tree/summary-zz-extra-files/css-files)


## Setup & Analyzing the Project Folder 06:30
- python --version
    ==> Python 3.9.1
## 0:10:32 – Setting Up the Development Environment 

## 0:12:33 – Creating Your First Django Project
- md django_course_env
- cd django_course_env
## Create a djangle project in curent folder
- python pip install Django
### start django project
- django-admin startproject django_course_site .
### run the web server
- python manage.py runserver [9000]
    - here 9000 is otonal if not specified 8000 is default
## 0:18:44 – Using the Integrated Terminal in VSCode 
- stop the web server by pressing ctrl+C
- View > command palette
    - type python interpreter
    - hear vscode use globaly installed interpreter
        - but we wat to use the one in vertual enviorenment
        - type: pipenv --venv
            - C:\Users\Ranjithj\.virtualenvs\storefront-Api0WwI4
            - copy this path to select interpreter box
                - C:\Users\Ranjithj\.virtualenvs\storefront-Api0WwI4 ***\bin\python***

## 0:12:33 – Creating Your First Django App
- open the settings.py 
    - got INSTALLED_APPS section
    - delete 'django.contrib.sessions',  which we dont need
### create app
- python manage.py startapp meetups
    - new folder has been created meetups by name
### registering the app
- got INSTALLED_APPS section
    - add 'playground'   at the bottom
## 0:25:36 – Writing Views
- open the views file and add lines as requered
- now we have to map thease view to urls file in order to view in the web browser
## 0:27:27 – Mapping URLs to Views
- in the plyground folder add new file as urls.py
- now we have to add the URL Conf to main urls file in the storefront>urls.py
## Templates rendering
- create new folder meetups>templates
    - create new folder meetups>templates>meetups
        - create new file meetups>templates>meetups>index.html
- inthis index file
    - type ! and press tab
    - you wil get html code skelton
    - change index, views files as needed
## applynig css and jscript in html files
- css and js not influened by djago or pytho. . it shows as it is
- create folder static under meetups
    - this holds all your sttic files like img, css etc. . 
 - create sub folder meetups under static

     <link rel="stylesheet" href="base.css">
   <link rel="stylesheet" href="{% sratic 'meetups/styles/base.css' %}">

## Vesioning and push to gihub heare after
### prepare remote rpo
- Repository name: django_course_env
- Description: Python Django Course for Beginners 2021 - Learn Django from Scratch in this 100% Free & Tutorial
- .gitignore: .gitignore Python
- [Github url](https://github.com/ranjithjaya/django_course_env.git) 

### Local Setup
- $ cd django_course_env
- $ git init
- $ git status
### check the Alias
    - $ git remote -v
### Remove Alias if needed
    - $ git remote remove origin
    - $ git remote -v
### Set Alias for the remote rpo-url
    - $ git remote add origin https://github.com/ranjithjaya/django_course_env.git
    - $ git remote -v
### Commit changes to local rpo area
    - $ git add .
    - $ git commit -m "initial add all files"
### Push local rpo to remote rpo
    - git push -u origin master

## 01:51:46 Getting Started with Models 
### Commit changes to master as ver-1
    - $ git add .
    - $ git commit -m "End of ver-1 before data base definition"
### Create branch for ver-1
    - $ git branch ver-1
### Create branch for ver-2
    - $ git add .
    - $ git commit -m "Begging of ver-2 before data base definition"
### edit the model.py    
- open the models.py file and add the followings
````Python
from django.db import models

class Meetup(models.Model):
    title = models.CharField(max_length=200)
    # organizer_email = models.EmailField()
    # date = models.DateField()
    slug = models.SlugField(unique=True)
    description = models.TextField()
    # image = models.ImageField(upload_to='images')
    # location = models.ForeignKey(Location, on_delete=models.CASCADE)
    # participants = models.ManyToManyField(Participant, blank=True, null=True)
````
# Development 2nd stage
- Date: 03-Sep-21
- pull the src from
    - [academind/django-practical-guide-course-code Branch: summary-06-using-template-inheritance](https://github.com/academind/django-practical-guide-course-code/tree/summary-06-using-template-inheritance)
    - cd django_course_env_ver-06
    - $ git pull origin summary-06-using-template-inheritance
## push to remote repo
    - Repository name: django_course_env
    - Description: Python Django Course for Beginners 2021 - Learn Django from Scratch in this 100% Free & Tutorial
    - Repo url: https://github.com/ranjithjaya/django_course_env.git
    - Branch: ver-06-before-work-with-DB
## check the Alias
    - $ git remote -v
### Remove Alias if needed
    - $ git remote remove origin
    - $ git remote -v
### Set Alias for the remote rpo-url
    - $ git remote add origin https://github.com/ranjithjaya/django_course_env.git
    - $ git remote -v
### Commit changes to local rpo area
    - $ git add .
    - $ git commit -m "Beginning of ver-6 before work wit DB"
### Push local rpo to remote rpo
    - git push -u origin master
