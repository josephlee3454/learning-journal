### <!DOCTYPE html>
#### <html>
   ### <head>
### <title>Constructive &amp; Co.</title>
###        <link rel="stylesheet" href="starter-code/css/c01.css"/>

  ###  </head>
### <body>
###        <h1>Constructive &amp; Co.</h1>
   ###     <script src="add-content.js"></script>
   ### <p> For all orders and inquries please call</p>
### <em>555-3344</em>
   ### </body>
### </html>
### var today = new Date();
### var hourNow = today.getHours();
### var greeting;
### if (hourNow > 18) 
### {
### greeting = 'good evening joe';
### }else if (hourNow > 12)
### {
### greeting = 'good afternoon joe';
### }
### else if (hourNow > 0)
### {
### greeting = 'good morning joe';
  ###  }
### else {greeting = 'welcome joe';}
###    document.write('<h3>' + greeting + '</h3>');
* The main take away i learned was how to iterpet what the code says on javascript above basically it says if it is past 1800 the program will say good evening, if it is past noon the program will say good afternoon , after midnight it will say good morning, and if noine of the values apply it will just say elcome joe
 

