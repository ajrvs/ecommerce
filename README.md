# ecommerce
Building an E-commerce website.

`virtualenv env`

`env\Scripts\activate`

`pip install Django`

`django-admin startproject ecommerce .`

`python manage.py startapp store`

add app (store) to INSTALLED_APPS within settings.py ("store.apps.StoreConfig")

run `python manage.py runserver` and open port 8000 to see default django landing page, which confirms that everything is setup correctly

now that store app is configured correctly, let's create templates folder

file structure should look like this appname (store) --> templates --> appname (store)

create templates: main.html, store.html, cart.html, checkout.html

main.html → Template which all will inherit from
store.html → Home page/store front with all products
cart.html → Users shopping cart
checkout.html → Checkout page

for now, add on the name of each page in h3 tags so we can test them

