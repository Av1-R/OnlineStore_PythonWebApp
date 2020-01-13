The Structure (CVM: Controller, View, Model):
=============================================


model.js
--------

Retrieves data from an api like host at /products & /cart and stores the data locally in two classes Products() and
Cart(). The model module primarily contains functions that manipulate data (sorting functions), GET & POST requests.



index.js (Controller)
---------------------

This module is concerned with user interaction and event handling when a user clicks elements on the page. This also
works as an intermediary between index.html and the model module. This is because it finds data input in the View
module (index.html) and passes it into functions in the model module which then performs the appropriate functionality.


index.html (View)
-----------------

This file is concerned with displaying information to the user. All user input forms are defined in this file and is
used


User Interaction & Functionality:
=================


Displaying a selected product
------------------------------

The main page at "/" displays a list of all products available to users. Users can pick a product they would like
to view by clicking the product name. This will trigger the .click functions in index.js that retrieve data from
model.js and display it on the page through the scripts in index.html.


Sorting the product list
-------------------------

There are functions defined in model.js that are called by index.js when the user clicks on either the table header
for Products and Cost that sort by the selected attribute. E.g. if Products is clicked, the list will be displayed in
alphabetically ascending order by product name.


View Cart & Refresh Cart
------------------------

These are both simply elements on the page which the user can click to either display or update the cart to show
recent and more accurate values. Both these buttons call upon functions in all 3 modules.


Modify Cart
-----------
The cart can be modified due to two forms available in the cart. One can update the current quantity of the selected
item to a new value and the other (remove) will remove all instances of the selected item in the cart. Both these
features like many others use functions present in all modules. In this case a POST request from the Cart() class
is used to update the cart.
