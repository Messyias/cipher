# Guide Three: Thugify

## Introduction

### What is Thugify?

Thugify is an introduction to the basics of Javascript

We'll be adding ", dawg" to the end of whatever you type into an input box — simple, but sweet. You'll be able to change the word added at your own will.

For example, you can customize this to make it Politify, which adds ", please" instead

This slide deck created by Amy Sorto and modified by [Cipher](http://projectcipher.io) is a great introduction to key concepts. Please take a look through it [here](https://docs.google.com/presentation/d/1N2l9FTYlGCocr8cqjLaHpp5tgv0hS-WI3US7PiMbRnc/edit)!

### Resources

Code: [https://ide.c9.io/jevinsidhu/thugify](https://ide.c9.io/jevinsidhu/thugify)

Final Webpage: [http://jevinsidhu.github.io/thugify](http://jevinsidhu.github.io/thugify)

## Workspace Setup

### Create Your Files

1. create a `index.html` file
2. create a `style.css` file
3. create a `script.js` file

## Setting Up Your HTML File

If you don't remember the basic structure of an HTML file, take a look at the [Personal Website](https://learn.projectcipher.io/guides/personal_website/) guide!

In this guide, we will cover connecting the CSS and JavaScript file, and nothing else. However, the finished structure is at the end of this "Setting Up Your HTML File" section.

### Connecting the Files

We need to connect the HTML file to the CSS and JavaScript files.


#### CSS
Let's connect our CSS file first: `<link href="style.css" rel="stylesheet">`

This line creates a `link` tag that should be placed in between the `<head>` and `</head>` tag. It describes:

* The location of the CSS file with the attribute `href`
* That we are linking a "stylesheet", or CSS file with the attribute`rel`


#### JavaScript
Next, connect our JavaScript file: `<script src="script.js">` 

This line is **linking the HTML file to the JS file**, just like we link CSS.

It creates a `script` tag that is placed right before the `</body>` tag.

* Webpages + browsers are really dumb, humans just make them smart
* `<script>` is a tag that links the HTML file to the JavaScript file
  * `src` is called an **attribute**
    * It **specifies the location** — in this case it was simply the file name, _“script.js”_ 

```
<!DOCTYPE html>
<html>
  <head> 
    <link href="style.css" rel="stylesheet">
  </head>

  <body> 

    <script src="script.js"> </script>
  </body>

</html>
```

### Create the HTML Structure

Our focus for this workship is the basics of JavaScript. Let's finish up our HTML first!  

First, create a `<div> </div>` tag.

This is a container to:

* organize our content
* apply styling from our **style.css** file to everything enclosed

```
<div>

</div>
```

Next, add the name of the workshop; let's create a `<h1> </h1>` header tag.

Give the header tag an id of "title".

* Type `id="title"` before the `<h1` is closed

It should look like this: `<h1 id="title"> Thugify </h1>`

* I.e. there may be multiple `<h1>` tags in your code. To select one it needs to have its custom name, thus the id

Indent your code!

* Indenting items that are enclosed within another tag is important for your own readability
  * In this case `<h1>` is enclosed in `<div>`

```
<div class="thugin"> 
<h1 id="title">Thugify</h1>     
</div>
```

Unidented

```
<div class="thugin"> 
  <h1 id="title">Thugify</h1>     
</div>
```

Indented

Isn't that easier to read?

**3. Let's create a place to input our text with the **`<input>`** self-enclosed tag**

`<input>` is a **self-enclosed tag** for creating an **input box.**

We'll be able to type in this box!

![](https---d2mxuefqeaa7sj.cloudfront.net-s_E2C9EC3A53C7D3F150F7715638F7F1B7BEFDBDD43B2CBAF8BECDEE9CE6CD10B0_1449368504615_Screen+Shot+2015-12-05+at+9.21.34+PM.png)

Give this input box an **id of "texter"**  
`<input id="texter">`

We can give the box **"placeholder text"** as well~

* Placeholder text is the greyed out text \(see the picture above\)

Add a `placeholder`** attribute** \(like `src` is an attribute\);

* `placeholder="some text"` _right after the id_

`<input id="texter" placeholder="insert text">`

We've made the place holder simply say "insert text"

**4. Let's make a submit button with the **`<button>`** tag**

`<button>` is the tag for creating a button

* Just like the `<h1>` tag, this is another tag where we place text between the opening and closing tags to display on the webpage

Give this button the **text " thugin' "**

`<button> thugin' </button>`

Give this button an **id of "go"**

`<button id="go"> thugin'</button>`

We're going to tell the webpage that this is of **type-something**

* In this case, it's a **button**!

To do this, we're also going to give this a `type` attribute

[Another one](https://www.youtube.com/watch?v=Xdh0TeGNsTw) \(**attribute**\);

* type="button" _right before the id_
  * This is to ensure that the webpage understands we want a button
    * By specifying this, the HTML adds some build-in CSS styling

```
<div class="thugin"> 
  <h1 id="title"> Thugify</h1>  
  <button type="button" id="go"> thugin'</button>   
</div>
```

### _Look at that beautiful indenting. Is yours indented?_

![](http---i.imgur.com-qHEIc0k.gif)

**4. To create a space for our thugified content, let's create a **`<p>`** tag with an id of **`output`

`<p id="output"> </p>`

`<p>` stands for paragraph

* Just like the `<h1>` tag, this is another tag where we place text between the opening and closing tags to display on the webpage

Whatever text we type into the **input box** will have **", dawg"** added

* We will then add the text between the opening and closing `<p>` tags
  * We'll do this using **JavaScript**

Final Code \(**do not copy and paste, you bumface**\);

```
<body> 

<!-- Our main HTML -->
  <div class="thugin"> 
      <h1 id="title"> Thugify </h1>
      <input id="texter" placeholder="insert text">
      <button type="button" id="go"> thugin' </button>
      <p id="output"> </p>       
  </div>

<!-- Our JavaScript files, also referred to as simply "scripts" -->  
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>
  <script src="script.js"> </script>

</body>
```

## CSS

CSS \(cascading style sheets\) is the styling of our page

* This styling lives in the **style.css** file

We use selectors in CSS that select our HTML tags

We want **you** to style the page!

* If you feel uncomfortable, that's good! You'll only really grow by being put into uncomfortable situations and then figuring your way out

* Your peers are **here to help you** if you have any questions, **all you gotta do is ask**

  * **Google** is also amazing! it's what _**all programmers**_ turn to, especially **professionals**!

If you feel completely lost, no worries! Go back to our older workshops and skim through those \(linked at the top of this document\).


## Javascript, dawg

Remember that the variable names in the examples below can be **anything** you want, but we recommend sticking with ours in order to make the workshop easier to follow!

### Adding a Listener

To begin our JavaScript journey to [_Thug Land_](https://cloud.githubusercontent.com/assets/9014119/19824102/cb1a4db2-9d3a-11e6-9bcd-deed6783092a.png) we'll need to add a listener to listen for a click on the **Thugify** button.  
`document.getelementById('go')`

This line simply means: Find the element with the id **"go"** in the document.

Now we haven't done anything with this element yet, we want the button to trigger some code when someone presses it, so we'll add `.onclick = function() {}` to the end of the end of the line.

`.onclick` simply adds a rule to listen for a click on the button and runs whatever's behind it.  
In this case, `= function() {}` happens to be assigned to it.

With that known, we can infer that `.onclick = function() {}` simply means: When a click is registered, run the following function.

To review, so far our code is  
`document.getElementById('go').onclick = function() {}`  
which simply says: Find the element 'go' and listen for a click on this element. If there is a registered click, run this function.

If you've followed along this far, awesome! You're doing great, we're almost done. If you're stuck, turn to a peer! We a team and we the best.

.![](https---d2mxuefqeaa7sj.cloudfront.net-s_E2C9EC3A53C7D3F150F7715638F7F1B7BEFDBDD43B2CBAF8BECDEE9CE6CD10B0_1449382445802_5833673d42c72dd12cb4078eb757c92f.500x274x12.gif)

Now that we've gotten Javascript to listen for a click on the button, we need to tell it what to do when it gets a click.

### Creating a variable and assigning a value

Every line that we want to execute **needs** to be inside the curly brackets `function(){}`  
Don't forget to indent it either! Remember, it'll make it easier to read.

So let's start with first finding what we need to **thugify.**

**Remember from the **[**Slidedeck**](https://docs.google.com/presentation/d/1N2l9FTYlGCocr8cqjLaHpp5tgv0hS-WI3US7PiMbRnc/edit#slide=id.gd76540ddf_0_22)**: When creating variables \(var\), whatever is on the right side, is always being assigned to the left side.**

* I.e. `var div = content` 
* the content on the right is going to be assigned to the variable `div` on the left

**The id **`texter`** is from the input box!**

We'll be grabbing the value from the input box, since the id `"texter"` is assigned to the box

* Whatever someone types into the input box will be retrieved with this line of JavaScript

To do that we need to use:  
`var div = document.getElementById('texter').value;`

  
Means to take the **value of** the element `texter` and **store it into a new variable** called `div`

We're grabbing the value from the input box, since the id `texter` is assigned to the box

* Whatever someone types into the input box the text will be retrieved with this line of JavaScript.

We're gonna use this _**string**_ value to thugify later on.

* A string is a series of characters \(text and numbers!\)
  * This is also mentioned in the [Slidedeck](https://docs.google.com/presentation/d/1N2l9FTYlGCocr8cqjLaHpp5tgv0hS-WI3US7PiMbRnc/edit#slide=id.gd76540ddf_0_22)

So, we've debunked that mystery!

![](mystery.gif)

Let's move on to performing the actual **thugifying** part of the string we got in the last part. 🏀

### Adding the `", dawg"` to the `add` Variable

We need to store the variable with the words from the input box and then **add** the word `", dawg"` to it.

`var add = div + ", dawg";`

This line takes the string we got in the last section \(the variable div\) from the input box, and adds `", dawg"` to the end of it, and then stores it into a new variable named `add`

Adding the two strings together is called `Concatenation.` Ya fancy, huh?

![](steveharvey.gif)

Alrighty, now that we're **thugin'** it's time to display our up text on the page — fo'shizzle.

### Displaying the Text

We're going to use `document.getElementById()` to find an element on the HTML page by it's id

`document.getElementById('output')`

This will take care of that job for us

* We're finding the element with the id `output`

Syntax means the grammar, spelling and set of rules of a language

Now then, we will stick `.innerHTML = add;` to the end of the line

`document.getElementById('output').innerHTML`

We're setting the `innerHTML` value \(the text inside the pairs of `<p>` tags\) of an HTML element instead of getting a value from it.

Now we will assign the value of add to the `<p>` tag with the **id** of `output`

`document.getelementById('output').innerHTML = add;`

In plain English, this means:

* set the `innerHTML` of `"#output"` to the value of the **variable**, `add` \(our th_ugified string variable → the variable that holds our text_\)

Close your curly brackets of the function **\(**`}`**\)**, slap a semicolon **\(**`;`**\)** on the end of it and BAM you're done!

Final Code \(**do not copy-pasta you bumface**\):

```
document.getElementById('go').onclick = function() {
    var div = document.getElementById('texter').value;
    var add = div + ", dawg";
    document.getElementById('output').innerHTML = add; 
};
```

## You are now a JavaScript Legend.

![](http://i.imgur.com/BJiD03Q.gif)
