# css 
* works by associating rules with HTML elments. these rules govern how the content of specified elements 
should be displayed. css rules contains 2 parts a selector and a decleration.
### Example
#### p {font family: Arial;}
* the p in front of the curly brackets is the selector
* the declaration is the **font-family: arial;**

## css Declarations 
*CSS declarations sit inside curly brackets each is constructed with 2 parts property and value 
###Example
#### color:yellow;
* the color is the property and yellow is the value
* **note** you specify several properties in one declaration, each will have to be separted by a semi-colon


### External style sheets 
* An external style sheet is a separate file with a .css extension with all CSS style definitions 
for the HTML page(s). You give a reference to this file in the <link> tag inside the <head> 
in the HTML, as shown below:
##### <html>

  ##### <head>

##### <title>My webpage</title>
##### <link rel='stylesheet' type='text/css' href='mystyles.css'>

  ##### </head>

  ##### <body>

  ##### <h1>My Webpage</h1>

  ##### <p>Hello World! This is the first paragraph.</p>

  ##### <p class='jazzy'>This is the second paragraph.</p>

  ##### </body>

##### </html>
###  An external style sheet file called 'mystyles.css' containing all the styles needed for our HTML is below:

##### p {

   ##### font-size: 14px;

##### }

##### .jazzy {

   ##### background-color: red;

##### }

##### h1 {

##### text-decoration: underline;

#####    color: blue; } 

* [this example came from here](https://study.com/academy/lesson/external-style-sheets-in-css-definition-examples.html)
### Internal css style sheets 
* internal css is basically css rules within an html placement 
* for example:
##### <style>
##### body{
##### background-color:yellow;
#####  }
##### </style> 
* the internal css will be between the title


