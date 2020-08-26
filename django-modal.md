# Admin site
## Overview 
* The Django admin application can use your models to automatically build a site area that you can use to create, view, update, and delete records. This can save you a lot of time during development, making it very easy to test your models and get a feel for whether you have the right data. The admin application can also be useful for managing data in production, depending on the type of website.
* All the configuration required to include the admin application in your website was done automatically when you created the skeleton project (for information about actual dependencies needed, see the Django docs here). As a result, all you must do to add your models to the admin application is to register them. At the end of this article we'll provide a brief demonstration of how you might further configure the admin area to better display our model data.

## registering models
* First, open admin.py in the catalog application (/locallibrary/catalog/admin.py). It currently looks like this — note that it already imports django.contrib.admin:
### code
* from django.contrib import admin
##### register model here 
* Register the models by copying the following text into the bottom of the file. This code simply imports the models and then calls admin.site.register to register each of them.
### code 
* from .models import Author, Genre, Book, BookInstance
* admin.site.register(Book)
* admin.site.register(Author)
* admin.site.register(Genre)
* admin.site.register(BookInstance)

## Creating a superuser
* In order to log into the admin site, we need a user account with Staff status enabled. In order to view and create records we also need this user to have permissions to manage all our objects.  You can create a "superuser" account that has full access to the site and all needed permissions using manage.py.
### code
* python3 manage.py createsuperuser :this will create a ne super user and will have been added to the database. (restart server)
* python3 manage.py runserver


## Register a ModelAdmin class 
#### To change how a model is displayed in the admin interface you define a ModelAdmin class (which describes the layout) and register it with the model.
### code 
* admin.site.register(Author)
##### add author admin and registration 
* Define the admin class
* class AuthorAdmin(admin.
* ModelAdmin):
   * pass

#### Register the admin class with the associated model
* admin.site.register(Author, AuthorAdmin)

#### Now we'll add ModelAdmin classes for Book, and BookInstance. We again need to comment out the original registrations:
* admin.site.register(Book)
* admin.site.register(BookInstance)
#### Now to create and register the new models; for the purpose of this demonstration, we'll instead use the @register decorator to register the models (this does exactly the same thing as the admin.site.register() syntax):
##### Register the Admin classes for Book using the decorator
* @admin.register(Book)
* class BookAdmin(admin.
* ModelAdmin):
    * pass

# Register the Admin classes for BookInstance using the decorator
* @admin.register(BookInstance) 
* class BookInstanceAdmin(admin.ModelAdmin):
    * pass
#### Currently all of our admin classes are empty (see pass) so the admin behaviour will be unchanged! We can now extend these to define our model-specific admin behaviour.

## Configure list views
#### Configure list views
* The LocalLibrary currently lists all authors using the object name generated from the model __str__() method. This is fine when you only have a few authors, but once you have many you may end up having duplicates. To differentiate them, or just because you want to show more interesting information about each author, you can use list_display to add additional fields to the view. 
* Replace your AuthorAdmin class with the code below. The field names to be displayed in the list are declared in a tuple in the required order, as shown (these are the same names as specified in your original model).
### code
* class AuthorAdmin(admin.ModelAdmin):

*  list_display = ('last_name', 'first_name', 'date_of_birth', 'date_of_death')

#### For our Book model we'll additionally display the author and genre. The author is a ForeignKey field (one-to-many) relationship, and so will be represented by the __str__() value for the associated record. Replace the BookAdmin class with the version below.

* class BookAdmin(admin.ModelAdmin):
*  list_display = ('title', 'author', 'display_genre')
#### Unfortunately we can't directly specify the genre field in list_display because it is a ManyToManyField (Django prevents this because there would be a large database access "cost" in doing so). Instead we'll define a display_genre function to get the information as a string (this is the function we've called above; we'll define it below).
#### Add the following code into your Book model (models.py). This creates a string from the first three values of the genre field (if they exist) and creates a short_description that can be used in the admin site for this method.
### code
* def display_genre(self):
  * """Create a string for the Genre. This is required to display genre in Admin."""
        return ', '.join(genre.name for genre in self.genre.all()[:3])
    
    * display_genre.short_description = 'Genre'
## add list filters
#### Once you've got a lot of items in a list, it can be useful to be able to filter which items are displayed. This is done by listing fields in the list_filter attribute. Replace your current BookInstanceAdmin class with the code fragment below.
* class BookInstanceAdmin(admin.ModelAdmin):
   * list_filter = ('status', 'due_back')

## Controlling which fields are displayed and laid out
#### Update your AuthorAdmin class to add the fields line, as shown below (in bold):
* class AuthorAdmin(admin.ModelAdmin):
    * list_display = ('last_name', 'first_name', 'date_of_birth', 'date_of_death')
    * fields = ['first_name', 'last_name', ('date_of_birth', 'date_of_death')]