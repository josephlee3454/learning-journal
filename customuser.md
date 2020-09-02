# Django custom models
* Django ships with a built-in User model for authentication, however the official Django documentation highly recommends using a custom user model for new projects. The reason is if you want to make any changes to the User model down the road--for example adding a date of birth field--using a custom user model from the beginning makes this quite easy. But if you do not, updating the default User model in an existing Django project is very, very challenging.

# set-up 
* To start, create a new Django project from the command line. We need to do several things:
* $ cd ~/Desktop
* $ mkdir users && cd users
* $ pipenv install django==3.0.3
* $ pipenv shell
* (users) $ django-admin.py startproject config .
* (users) $ python manage.py startapp users
* (users) $ python manage.py runserver
# update models.py
#### from django.contrib.auth.models import AbstractUser
#### from django.db import models

#### class CustomUser(AbstractUser):
   #### pass
   #### add additional fields in here

    #### def __str__(self):
        #### return self.username

* We need new versions of two form methods that receive heavy use working with users. Stop the local server with Control+c and create a new file in the users app called forms.py.
#### (users) $ touch users/forms.py
* We'll update it with the following code to largely subclass the existing forms.
#### from django import forms
#### from django.contrib.auth.forms import UserCreationForm, UserChangeForm
#### from .models import CustomUser

#### class CustomUserCreationForm(UserCreationForm):

    #### class Meta:
        #### model = CustomUser
        #### fields = ('username', 'email')

#### class CustomUserChangeForm(UserChangeForm):

    #### class Meta:
        #### model = CustomUser
        #### fields = ('username', 'email')

* Finally we update admin.py since the Admin is highly coupled to the default User model.
#### from django.contrib import admin
#### from django.contrib.auth import get_user_model
#### from django.contrib.auth.admin import UserAdmin

#### from .forms import CustomUserCreationForm, CustomUserChangeForm
#### from .models import CustomUser

#### class CustomUserAdmin(UserAdmin):
    #### add_form = CustomUserCreationForm
    #### form = CustomUserChangeForm
    #### model = CustomUser
    #### list_display = ['email', 'username',]

#### admin.site.register(CustomUser, CustomUserAdmin)

* And we're done! We can now run makemigrations and migrate for the first time to create a new database that uses the custom user model.
#### (users) $ python manage.py makemigrations users
#### (users) $ python manage.py migrate
* superuser: It's helpful to create a superuser that we can use to login to the admin and test out login/logout. On the command line type the following command and go through the prompts.
#### (users) $ python manage.py createsuperuser
