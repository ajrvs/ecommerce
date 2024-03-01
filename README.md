# ecommerce
Building an E-commerce website.

## Steps

### Set up environment

`virtualenv env`

`env\Scripts\activate`

`pip install Django`

### Start project and configure app

`django-admin startproject ecommerce .`

`python manage.py startapp store`

add app (store) to INSTALLED_APPS within settings.py ("store.apps.StoreConfig")

run `python manage.py runserver` and open port 8000 to see default django landing page, which confirms that everything is setup correctly

### Templates

now that store app is configured correctly, let's create templates folder

file structure should look like this appname (store) --> templates --> appname (store)

create templates: main.html, store.html, cart.html, checkout.html

main.html → Template which all will inherit from
store.html → Home page/store front with all products
cart.html → Users shopping cart
checkout.html → Checkout page

for now, add on the name of each page in h3 tags so we can test them

### Views

create views and urls, and configure urls to base urls

> always check for typos

### Static files

create static files

file structure should look like this static --> css (main.css), images

in settings.py, add STATICFILES_DIRS and point it to the static folder we created, to specify additional directories from which static files should be collected during the [`collectstatic`](https://docs.djangoproject.com/en/5.0/ref/contrib/staticfiles/#collectstatic) management command

add static files (css file) to page (store.html)

`{% load static %}` template tag loads the static template and filters, allowing to use the `{% static %}` template tag to reference static files

`{% static %}` template tag generates the URL for static files (in this case, URL for the static file named 'css/main.css', located at static/css/main.css)

similarly add images/cart.png to page (store.html)

run the server to check if everything works as expected

### Main templates

clear store.html and add HTML boilerplate to main.html

give title "Ecom", add static file(s) and bootstrap

add {% extends 'store/main.html' %} to all the other pages (store.html, cart.html, checkout.html) as we want to inherit from main.html

make sure to use {% load static %} in all four html files

run the server to check

### Navbar

bootstrap navbar, dark theme, and customize it

custom css

### Store.html

this page will contain multiple rows and 3 columns per row of product information

create the layout in store.html file

may add dummy product(s) with information

### Cart.html

get HTML symbol code — [w3school](https://www.w3schools.com/charsets/ref_utf_arrows.asp)
