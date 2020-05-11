Ejs Partials
* partials are great when you want to reuse the same html across mutiple views
* pro tip think of partials as functions they bbuild large websites easier to to maintain as you dont have to go and change a peice of text in every page it appears instead all you do is define the reusable bundle of code in a file and includer it whereever you need it.



## Let’s go ahead and create those partials. Under the views/partials/ directory create a file callednavbar.ejs which will contain only the HTML for the navigation bar at the top of the home and post pages:



## Now our partials are defined, we can use them in our home.ejs and post.ejs templates! In EJS, any JavaScript or non-HTML syntax you include in your templates is always surrounded by <% %> delimiters.
## . You use <%- include( PARTIAL_FILE ) %> where the partial file is relative to the template  you use it in.

* The <%- %> tags allow us to output the unescaped content onto the page (notice the -). This is important to ude when using the include() statement since you don’t want EJS to escape your HTML characters like '<', '>', 
##  <!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8">
        <title>Node.js Blog</title>
        <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css">
        <style>
            body {
                padding-top: 20px;
                padding-bottom: 20px;
            }
            .jumbotron {
              margin-top: 10px;
            }
        </style>
    </head>
    <body>
        <div class="container">
            <%- include('partials/navbar') %>
            <div class="jumbotron">
                <h1>All about Node</h1>
                <p class="lead">Check out our articles below!</p>
            </div>
            <div class="row">
                <div class="col-lg-12">
                    <div class="list-group">
                      <!-- loop over blog posts and render them -->
                      LIST_OF_POSTS
                    </div>
                </div>
            </div>
            <%- include('partials/footer') %>
        </div>
    </body>
    </html>