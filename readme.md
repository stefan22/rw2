# FE Tools &nbsp; Bootstrap 4 &nbsp; :book:

## Notes &nbsp; :pencil2: &nbsp; :clipboard:
- ***col-auto***   
  + use enough columns to accomodate content - spreads up columns automatically   

- ***col*** and ***col-xx*** (col-sm, col-md)   
  + col and col-xx, are used onlhy once an initial value for a col and col-xx already been set   
    * it's use for remaining columns
    * col is just how the smallest col classes are now defined in bootstrap 4

- offset-1, offset-3  (just as with previous versions boostrap)   

- ***flex-last***, ***flex-first***     
  + allows you to reposition content in the same manner as with push and pull 

```
  ex:
  
    <div class="col-sm-3 col-md-4 flex-last">...</div>

    <div class="col-sm col-md flex-first">...</div>
```

- ul class of ***list-unstyled*** (this does the obvious)

```
  ex:
    <ul class="list-unstyled">...</ul>

```


- adding ***align-items-center*** to vertically aligns content within row


- ***justify-content-center*** (as oppose to the one above that vertically aligns the content)   
  + horizontally centers the column content within the row 
```
  ex:
    <div class="row justify-content-center">
     <div class="col-auto">

```

- also ***align-self-center*** which centers its entire content



- basic ***nav menu***

```
    <!-- collapses on sm inverse is black originally -->
    <nav class="navbar navbar-inverse navbar-toggleable-sm fixed-top">
        <div class="container">
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#Navbar">
                <span class="navbar-toggler-icon"></span>  
            </button>
            <a class="navbar-brand" href="#">RC¬®</a>
            <div class="collapse navbar-collapse" id="Navbar">
                <ul class="navbar-nav">
                    <li class="nav-item active"><a class="nav-link" href="#">Home
                    </a></li>
                    <li class="nav-item"><a class="nav-link" href="./aboutus.html">About
                    </a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Menu
                    </a></li>
                    <li class="nav-item"><a class="nav-link" href="#">Contact
                    </a></li> 
                </ul> 
            </div>   
        </div> <!-- endof container -->    
    </nav>


```


> I'm using `npm start`, to start lite-server and browsersync
>
<br/>


### breadcrumb syntax

```
      <ol class="col-12 breadcrumb">
            <li class="breadcrumb-item"><a href="./index.html">Home</a></li>
            <li class="breadcrumb-item active">About Us</li>
      </ol>

```

### icon fonts

font-awesome & bootstrap social

npm install font-awesome --save
boostrap-social.css

```
    <i class="fa fa-phone"></i>

    <a class="btn btn-social-icon btn-facebook" href="http://www.facebook.php?id=">

```
> you can use either span or i for font-awesome


> .hidden-xs-down =>hides div for xs and down

### user input:buttons and forms


```
    ex: button bar containing 3 buttons with an <a> tag

    <div class="btn-group" role="group">
        <a role="button" class="btn btn-primary" href="tel:+85212345678"><i class="fa fa-phone"></i> Call</a>
        <a role="button" class="btn btn-info"><i class="fa fa-skype"></i> Skype</a>
        <a role="button" class="btn btn-success" href="mailto:confusion@food.net"><i class="fa fa-envelope-o"></i> Email</a>
    </div>

```

### forms

- to divide the form into rows, apply the class ***form-group row***

```
    ex

        <form>
            <div class="form-group row">
                <label for="firstname" class="col-md-2 col-form-label">
                    First Name</label>
                <div class="col-md-10">
                    <input type="text" class="form-control" id="firstname" name="firstname" placeholder="enter firstname" />
                </div>    
            </div> <!-- first row -->

            <div class="form-group row">
                <label for="lastname" class="col-md-2 col-form-label">
                    Last Name</label>
                <div class="col-md-10">
                    <input type="text" class="form-control" name="lastname" id="lastname" placeholder="enter lastname" />
                </div>
            </div> <!-- second row -->

            <div class="form-group row">
                <label for="phone" class="col-md-2 col-form-label">Contact Tel.</label>
                <div class="col-md-10">
                    <input type="number" class="form-control" name="phone" id="phone" placeholder="enter telephone number">
                </div>

            </div><!--  third row -->

            <div class="form-group row">
                <label for="email" class="col-md-2 col-form-label">Email
                </label>
                <div class="col-md-10">
                    <input type="email" class="form-control" name="email" id="email" placeholder="enter email">
                </div>
            </div> <!-- fourth row -->

            <div class="form-group row">
                <label for="feedback" class="col-md-2 col-form-label">Your Feedback</label>
                <div class="col-md-10">
                    <textarea class="form-control" id="feedback" name="feedback" rows="12"></textarea>
                </div>
            </div><!--  fifth row -->

            <div class="form-group row">
                <div class="offset-md-2 col-md-10">
                    <button type="submit" class="btn btn-primary">Send Feedback</button>
                </div>
            </div> <!-- sixth row -->

        </form>

```

### tables
- start by assigning them a class of table

```
        ex:
        <table class="table">
            ...
        </table>
```

***table-stripped*** -> for zebra stripped rows

***table-bordered*** -> for borders to table cells

***table-hover*** for highlighting rows when you hover over a row

***table-sm*** for cutting the cell padding in half

***table-responsive*** for making responsive tables

#### Color tables:
    
- with following classes: active, success, info, warning, danger

```
        ex:

        <tr class="bg-success">..</tr>
        <tr class="bg-danger">..</tr>
```

### images

```
    ex: nav-brand

    <a class="navbar-brand" href="/.index.html">
        <img src="images/bird.png" width="40" height="40" class="img-fluid">
    </a>

```

```
    ex: media object - class of mr-3 is margin-right 3
        and mt-0 is margin top zero
        d-flex allows u to position the image

    <div  class="col-sm col-md-12">
        <div class="media">
            <img class="d-flex mr-3 img-thumbnail align-self-center"
                 src="images/restaurant.jpg" />
            <div class="media-body">
                <h2 class="mt-0">Upizza</h2>
                <p>A unique combination of Indian Uthappam (pancake) and Italian pizza, topped with Cerignola olives, ripe vine cherry tomatoes, and Buffalo Paneer.</p>
            </div>
        </div>
    </div>    



```

### badges

```
    ex: added two badges to an h2 tag

    <h2 class="mt-0">Upizza 
        <span class="badge badge-danger">HOT</span> 
        <span class="badge badge-pill badge-default">$4.99</span>
    </h2>

    * first one is of a rect shape red and the second one is gray rounded.

```

### javascript components in bootstrap

- css classes with js support using ***data attributes***

```
    ex:
        data-toggle, data-spy
```

#### tabs 

-  tabbed navigation -> for organizing content
-  tab panes -> organize content into panes

```
    ex:

        <ul class="nav nav-tabs">
            <li class="nav-item">
              <a class="nav-link active" href="#peter"
                role="tab" data-toggle="tab">Peter Pan, CEO</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#danny" role="tab"
                data-toggle="tab">Danny Witherspoon, CFO</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#agumbe"role="tab"
                data-toggle="tab">Agumbe Tang, CTO</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#alberto" role="tab"
                data-toggle="tab">Alberto Somayya, Exec. Chef</a>
            </li>
        </ul>

        <div class="tab-content">
            <div class="tab-pane fade show active" id="peter">
                <h4>Peter Pan <small>Chief Epicurious Officer</small></h4>
                <p>Our CEO, Peter, credits his hardworking East Asian immigrant parents who undertook the arduous journey to the shores of America with the intention of giving their children the best future. His mother's wizardy in the kitchen whipping up the tastiest dishes with whatever is available inexpensively at the supermarket, was his first inspiration to create the fusion cuisines for which <em>The Frying Pan</em> became well known. He brings his zeal for fusion cuisines to this restaurant, pioneering cross-cultural culinary connections.</p>        
            </div> <!-- tab-pane -->

            <div class="tab-pane fade"  id="danny">
                <h4>Dana Shass <small>Chief Food Officer</small></h4>
                <p>Our CFO, Danny, as he is affectionately referred to by his colleagues, comes from a long established family tradition in farming and produce. His experiences growing up on a farm in the Australian outback gave him great appreciation for varieties of food sources. As he puts it in his own words, <em>Everything that runs, wins, and everything that stays, pays!</em></p>    
            </div>
        </div>    



        notes:
        ======

        * <ul> tag with nav and nav-tabs classes to setup navigation
        * each list-item is a tab
        * ids with <a> tags to set page anchors
        * data-toggle attribute inside <a> tag
        * active is the open tab





```


### collapse javascript plugin with card to create accordion to show/hide content

```
    ex: accordion

    <div id="accordion">
        <div class="card">
            <div class="card-header" id="peterhead">
                <h3 class="mb-0">
                    <a data-toggle="collapse" data-parent="#accordion"
                       href="#peter">
                       <h4>Peter Pan <small>Chief Epicurious Officer</small></h4>
                    </a>    
                </h3>
            </div>
            <div class="collapse show" id="peter">
                <div class="card-block">
                    <p class="hidden-xs-down">
                        Our CEO, Peter, credits his hardworking East Asian immigrant parents who undertook the arduous journey to the shores of America with the intention of giving their children the best future. His mother's wizardy in the kitchen whipping up the tastiest dishes with whatever is available inexpensively at the supermarket, was his first inspiration to create the fusion cuisines for which <em>The Frying Pan</em> became well known. He brings his zeal for fusion cuisines to this restaurant, pioneering cross-cultural culinary connections.
                    </p>
                </div>    
            </div>
        </div> <!-- endof card -->
    ..
    ....
    </div> <!-- endof accordion -->


    note: 
        * mb-0 it's just another bootstrap class /margin-bottom 0
        * hidden-xs-down -> won't show from xs and below


```


### scrollspy plugin
- regular <a href="#"> anchors within a page

```
    ex:

        body {
          position: relative;
        }

        //Add these two data attributes:
        <body data-spy="scroll" data-target="#top">

        //then:
        <div class="col-12 col-sm-12">
            <div class="top">
                    <a href="#top">TOP</a>
            </div>
        </div>  


        note: it says to add position relative to the body - it works without it too

```    



### tooltips, popups, and modals

- tooltips - when user hovers over an area
- popups - when user clicks on a link or a button
- modals - hide or show its content when user clicks on a link or a button






<kbd>nav menu</kbd>
<br/>
![](images/iphone6.png)

<kbd>screenshot two</kbd>
<br/>
![](images/iphone6-landscape.png)


> this alpha version of bootstrap throws an error 'collapse is transitioning'


      
