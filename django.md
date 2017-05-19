# Django 

### Creating a Project
* `$ django-admin startproject mysite` 
* `python manage.py startapp name-of-app`

### URL Mapping
* `url(regex, views, kwargs, name)`
* regex: doesn't search GET/POST or domain name 
* view: when regex match found, specified view function will be called 
* name: can refer to URL unambiguously elsewhere in Django

### Databases
* create tables before use: `python manage.py migrate`
* make changes to model: 
	* change model.py
	* run `$ python manage.py makemigrations` to create migrations for changes
	* run `$ python manage.py migrate` to apply changes to database

### Models 
* `model.py`: used to specify database layout 
```
class Question(models.Model):
    question_text = models.CharField(max_length=200)
    pub_date = models.DateTimeField('date published')


class Choice(models.Model):
    question = models.ForeignKey(Question, on_delete=models.CASCADE)
    choice_text = models.CharField(max_length=200)
    votes = models.IntegerField(default=0)
```

### Python Shell 
* to run: `$ python manage.py shell`
* use double underscore to separate relationships 

### Database Lookup API
* `class.objects.filter()`
	* parameters: id=1, question_text__startswith='What'
* `Question.objects.get()`
	* parameters: pub_date__year=current_year, id=2
* `.create()`: create an object
* `.delete()`: delete an object 

### Django Admin
* used by site managers 
* create admin account: `python manage.py createsuperuser`

### Views
* return HttpResponse object containing requested page or exception such as Http404
* `render()`: request object as first argument, template name as second argument, dictionary as third argument 
* `get_object_or_404()`: takes django model as first argument and arbitrary number of keyword arguments 

### Context
* dictionary that maps template variable names to Python objects 
