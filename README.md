# 201 Day 2

HTML5 Layout Elements
-------------------------
In HTML5, a new set of elements were established to allow you to better structure your page, vice having 20 thousand <divs> all wrapped inside of each other.

`<header>` , `<nav>` , `<article>` , `<aside>` , `<footer>` , `<section>` , `<hgroup>` , `<figure>` , `<figcaption>`

* header is the header of the page
* nav is the navigational bar
* article is your main content
* aside can be in or out of your article, depending on what you want it to display
* footer is the footer of the page
* section groups related together inside of your article
* hgroup allows <h1> <h2> <h3> tags to be grouped together so they are one single heading
* figure is used to contain any content that is referenced from the main flow of an article i.e. pictures, videos, graphs...
* figcaption sits inside of figure and is the caption of that content


```
                                          v concatination
Concatinated Sentence : alert('Greetings' + userName+ '!');
                                 ^string       ^variable
```

Datatypes - Variables, Strings and Nums
`typeof` will tell you the data type of a variable

# 201 Day 3
## Lists!

`<ol>` is ordered lists, meaning 1. 2. 3.
`<ul>` is unordered lists, meaning * * *
`<dl>` is definition lists, kind of how you'd read a definition in the dictionary.  It's structured different from the other two.

Example of `<ol>`
```
<ol>
  <li>Item #1</li>
  <li>Item #2</li>
</ol>
```

Example of `<ul>`
```
<ul>
  <li>Bullet #1</li>
  <li>Bullet #2</li>
</ul>
```

Example of `<dl>`
```
<dl>
  <dt>Definition Lists</dt>
    <dd>The definition list is created with a <dl> element and usually consists of a series of terms and their definitions.</dd>
  <dt>Unordered Lists</dt>
    <dd>The unordered list contains a list of items that start out with billet points.</dd>
</dl>
```

Example of nested lists, meaning it's a list inside of a list!
```
<ul>
  <li>French Fries</li>
  <li>Hamburger</li>
    <ul>
	  <li>Cheese</li>
	  <li>Hamburger Patty</li>
	  <li>Ketchup</li>
	  <li>White Buns</li>
	</ul>
  <li>Large Coke</li>
</ul>
```
# Boxes
Everything in HTML is just made up of boxes and you can even place boxes inside of boxes.  When you build the initial framework for your site, it's best that you just write all of your HTML content first and make sure that your boxes contain what they need in them, then you can apply CSS to those boxes and make them pretty much do whatever.... after a few hours of praying to the CSS gods.


## Setting the size of your box

By default, a box is just large enough to hold it's contents.  You can define the properties of said box though, which is generally a good idea.  The properties listed below can have a few different ways of setting the values - `auto`, `length (which is px, cm, etc)`, `%`, `initial`, and `inherit`.

property | explanation
-------- | -----------
height | sets the height of the element
width | sets the width of the element
min-width | sets the minimum width of the element
min-height | sets the minimum height of the element
max-width | sets the maximum width of the element
max-height | sets the maximum height of the element

## Other properties for your box

This is just a general list of other properties in no specific order.

property | explanation
-------- | -----------
overflow | requires either `hidden` or `scroll` value.  Tells the box what to do with this content if it's larger than it's container.
border | Separates the edge of the box from another.  You can also 'shorthand' the border by writing the width, style and color in one line. `border: 3px dotted #0088dd;`
margin | sits outside the edge of the border
padding | space between the border of a box and any content contained within it
border-width | requires either `thin`, `medium`, `thick` or a pixel value.  Used to control the width of a border.
border-style | requires either `solid`, `dotted`, `dashed`, `double`, `groove`, `ridge`, `inset`, `outset`, or `hidden`.  Used to control the style of the border, can also be applied individually to each corner using `border-top-style` `border-left-style` etc.
border-color | requires RGB, hex or CSS colors.  Sets the color of the border.
border-image | Applies an image to the border of any box.  It takes a background image and slices it into nine pieces.
display | requires `inline`, `block`, `inline-block`, or `none`.
display: inline | This causes a block-level element to act like an inline element
display: block | This causess an inline element to act like a block-level element
display: inline-block | This causes a block-level element to flow like an inline element, while retaining other features of a block-level element
display: none | This hides an element from the page
visibility | requires either `hidden` or `visibile` and does exactly what you think
box-shadow | Allows you to add a drop shadow around a box.  This one confuses me.
border-radius | This allows the ability to create rounded corners on any box!

---

## if/else statements

The if...else statement checks a condition.  If I'm equal to something, do X else do Y.  You can involve a ton of logic into if else statements and go pretty deep into the rabbit hole if you want!

```
  var amIHappy = 'Yes';

  if (amIHappy === 'Yes') {
    alert('Yay!  Me too!');
  } else {
    alert('Oh no.. Please try to cheer up!');
  }
```

---

## switch statements

Switch statement starts with a variable called the switch value.  Each case indicates a possible value for this variable and the code that should run if the variable matches the value.
```
switch (level) {
  case 'One':
    title = 'Level 1';
    break;
  
  case 'Two':
    title = 'Level 2';
    break;

  case 'Three':
    title = 'Level 3';
    break;
}
```
---

## if/else vs switch

if/else does not require an `else`, you can just do `if (something) { } if (somethingelse) { }` but each statement is checked as it goes along, so if it's a super indepth process, it may be slow.

switch has a default option that is run if nothing matches, and if a match is found it immediately goes to that and breaks the code, so if it's a super indepth process, it may be fast.

---

## Arrays

Arrays are basically a massive list of ordered data, starting at 0.

```
var favFoods = ['Miso Ramen', 'Tuna Roll', 'Chicken Katsu', 'Steak'];

console.log('My favorite food is ' +favFoods[0]);
console.log('My second favorite food is ' +favFoods[3]);
console.log('I really enjoy eating ' +favFoods[1]+ ' with ' +favFoods[2]+'.');

favFoods[4] = 'Rice';

console.log('Sometimes though, I would eat ' +favFoods[4]+ ' for breakfast.')
```

## Loops

This example utilizes the above array
```
for(var i=0; i < favFoods.length; i++;) {
  console.log(favFoods[i]);
}
```

```
for(var i=0; i < favFoods.length; i++;) {
  if(favFoods[i] === 'Miso Ramen') {
    console.log(favFoods[i]);
    break;
  }
}
```
This loop displays any even result within the array.  The % in this is called a mod, or modifier.
```
for(var i=0; i < favFoods.length; i++) {
  if (i % 2 === 0) {
    console.log(favFoods[i]);
  }
}
>> Miso Ramen
>> Chicken Katsu
```
This loop will display everything that's not equal to Malaki
```
var myPets = ['Tangerine', 'Malaki','Cookie'];

var i=0;

while(i < myPets.length) {
  if (myPets[i] !== 'Malaki') {
  console.log(myPets[i]);
  i++;
  } else {
  i++;
  }
}
```
