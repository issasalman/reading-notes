#  Django Models


Django web applications access and manage data through Python objects referred to as models. Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms, etc.

## Designing the LocalLibrary models
* When designing your models it makes sense to have separate models for every "object" (a group of related information). In this case, the obvious objects are books, book instances, and authors.

* You might also want to use models to represent selection-list options (e.g. like a drop down list of choices), rather than hard coding the choices into the website itself — this is recommended when all the options aren't known up front or may change. Obvious candidates for models, in this case, include the book genre (e.g. Science Fiction, French Poetry, etc.) and language (English, French, Japanese).

* Once we've decided on our models and field, we need to think about the relationships. Django allows you to define relationships that are one to one (OneToOneField), one to many (ForeignKey) and many to many (ManyToManyField).

![model](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models/local_library_model_uml.svg)

## Model definition
Models are usually defined in an application's models.py file. They are implemented as subclasses of django.db.models.Model, and can include fields, methods and metadata. The code fragment below shows a "typical" model, named MyModelName:
```
from django.db import models

class MyModelName(models.Model):
    """A typical class defining a model, derived from the Model class."""

    # Fields
    my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')
    ...

    # Metadata
    class Meta:
        ordering = ['-my_field_name']

    # Methods
    def get_absolute_url(self):
        """Returns the url to access a particular instance of MyModelName."""
        return reverse('model-detail-view', args=[str(self.id)])

    def __str__(self):
        """String for representing the MyModelName object (in Admin site etc.)."""
        return self.my_field_name

```

### Fields
A model can have an arbitrary number of fields, of any type — each one represents a column of data that we want to store in one of our database tables. Each database record (row) will consist of one of each field value. Let's look at the example seen below:
```
my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')

```
### Common field types
1. CharField
2. TextField
3. IntegerField
4. DateField and DateTimeField
5. EmailField
6. AutoField
7. ForeignKey

### Metadata
```
class Meta:
    ordering = ['-my_field_name']
```
### Methods
A model can also have methods.

```
def __str__(self):
    return self.field_name
```
```
def get_absolute_url(self):
    """Returns the url to access a particular instance of the model."""
    return reverse('model-detail-view', args=[str(self.id)])
```

### model types
1. Genre model
2. Book model
3. BookInstance model
4. Author model

# Django Admin

The Django admin is a powerful built-in tool giving you the ability to create, update, and delete objects in your database using a web interface. You can customize the Django admin to do almost anything you want.

In this course, you learned how to:

* Register your object models with the Django admin
* Add attributes as columns in the change list
* Create column values with calculated content
* Cross-reference admin pages through links
* Filter the change list page through query strings
* Make your change list searchable
* Customize the automatic ModelForm object
* Change the HTML in Django admin templates


