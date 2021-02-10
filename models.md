1. #### Correct Model Naming
`It is generally recommended to use singular nouns for model naming, for example: User, Post, Article.
That is, the last component of the name should be a noun, e.g.: Some New Shiny Item. 
It is correct to use singular numbers when one unit of a model does not contain information about several objects.`

2. #### Relationship Field Naming
`For relationships such as ForeignKey, OneToOneKey, ManyToMany it is sometimes better to specify a name. Imagine there is a model called Article, 
— in which one of the relationships is ForeignKey for model User. If this field contains information about the author of the article, 
then author will be a more appropriate name than user.`

3. #### Correct Related-Name
`It is reasonable to indicate a related-name in plural as related-name addressing returns queryset. Please, do set adequate related-names. 
In the majority of cases, the name of the model in plural will be just right. For example:`
```
class Owner(models.Model):
    pass
class Item(models.Model):
    owner = models.ForeignKey(Owner, related_name='items')
```
4. #### Attributes and Methods Order in a Model
`Preferable attributes and methods order in a model (an empty string between the points).`

* constants (for choices and other)
* fields of the model
* custom manager indication
* meta
* def __unicode__ (python 2) or def __str__ (python 3)
* other special methods
* def clean
* def save
* def get_absolut_url
* other methods

5. #### BooleanField
`Do not use null=True or blank=True for BooleanField. It should also be pointed out that it is better to specify default values for such fields.
If you realise that the field can remain empty, you need NullBooleanField.
`

6. #### Business Logic in Models
`The best place to allocate business logic for your project is in models, namely method models and model manager.`

7. #### Do not use ObjectDoesNotExist
`Using ModelName.DoesNotExist instead of ObjectDoesNotExist makes your exception intercepting more specialised, which is a positive practice.`

8. #### . Use of choices
`keep strings instead of numbers in the database (although this is not the best option from the point of optional database use,
it is more convenient in practise as strings are more demonstrable, which allows the use of clear filters with get options from the box in REST frameworks).`

9. ####  Many flags in a model?
`If it is justified, replace several BooleanFields with one field, status-like. e.g.`

For more you macy check 
[best-practices-working-with-django-models](https://steelkiwi.medium.com/best-practices-working-with-django-models-in-python-b17d98ab92b)
