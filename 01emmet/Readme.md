# EMMET CHEETSHEET
``
Emmet is a web-developer’s toolkit that can greatly improve your HTML & CSS workflow. Emmet takes the snippets idea to a whole new level: you can type CSS-like expressions that can be dynamically parsed, and produce output depending on what you type in the abbreviation.
``


- # HTML 5 Boiletplate 

Syntax
> ! < tab >

### Output
```HTML
<!DOCTYPE html>
 <html lang="en">
 <head>
 <meta charset="UTF-8" />
 <title>Document</title>
 </head>
 <body>

 </body>
 </html>
```


 - # HTML tags
 ``Emmet doesn’t have a predefined set of available tag names, you can write any word and transform it into a tag: div -> <div></div> foo <foo></foo> and so on.
 ``
 
 Syntax
> tagname < tab >


### Output
```html
<body></body>
```
- # Child: >
``You can use > operator to nest elements inside each other:
``

```html
nav>ul>li < tab >

    <nav>
        <ul>
            <li></li>
        </ul>
    </nav>
```
- # Sibling: +
``
Use + operator to place elements near each other, on the same level:
``
```html
div+p+bq < tab >

 <div></div>
 <p></p>
 <blockquote></blockquote>
```
- # Climb up: ^

``
With > operator you’re descending down the generated tree and positions of all sibling elements will be resolved against the most deepest element:
``
```html
div+div>p>span+em^bq
 
 <div></div>
 <div>
 <p><span></span><em></em></p>
 <blockquote></blockquote>
 </div>

div+div>p>span+em^^bq
 
 <div></div>
 <div>
 <p><span></span><em></em></p>
 </div>
 <blockquote></blockquote>
```

- # Multiplication: *
``With * operator you can define how many times element should be outputted``
```html
ul>li*5

 <ul>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
 </ul>
 ```

 - # Grouping: ()
``
Parenthesises are used by Emmets’ power users for grouping subtrees in complex abbreviations.
``
```html
div>(header>ul>li*2>a)+footer>p
 <div>
    <header>
        <ul>
            <li><a href=""></a></li>
            <li><a href=""></a></li>
        </ul>
    </header>
    <footer>
        <p></p>
    </footer>
 </div>
 ```
- # ID and CLASS
``
In CSS, you use elem#id and elem.class notation to reach the elements with specified id or class attributes. In Emmet, you can use the very same syntax to add these attributes to specified element
``
```HTML
div#header+div.page+div#footer.class1.class2.class3

<div id="header"></div>
<div class="page"></div>
<div id="footer" class="class1 class2 class3"></div>
```
- # Item numbering: $
``With multiplication * operator you can repeat elements, but with $ you can number them. Place $ operator inside element’s name, attribute’s name or attribute’s value to output current number of repeated element:
``

```html
ul>li.item$*5
<ul>
    <li class="item1"></li>
    <li class="item2"></li>
    <li class="item3"></li>
    <li class="item4"></li>
    <li class="item5"></li>
</ul>
```
``With @ modifier, you can change numbering direction (ascending or descending) and base (e.g. start value).
For example, to change direction, add @- after $
``
```html
ul>li.item$@-*5
<ul>
    <li class="item5"></li>
    <li class="item4"></li>
    <li class="item3"></li>
    <li class="item2"></li>
    <li class="item1"></li>
</ul>
```
- # Text: {}
``
You can use curly braces to add text to element:
``
```HTML
a{Click me}

<a href="">Click me</a>
```
- # Lorem Ipsum generator
``
“Lorem ipsum” dummy text is used by many web-developers to test how their HTML templates will look with real data. 
``
```HTML
p>lorem10<!-- 10 words -->
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus, deleniti.</p>

```
- # Implicit tag names
``
    Some tags can be implicitly written using emmet abbrivation
``
```html
.class
     <div class="class"></div>

em>.class
     <em><span class="class"></span></
em>

ul>.class
     <ul>
        <li class="class"></li>
    </ul>

table>.row>.col
    <table>
        <tr class="row">
            <td class="col"></td>
        </tr>
    </table>
 ```
## [More about emmet](https://docs.emmet.io/cheat-sheet/)