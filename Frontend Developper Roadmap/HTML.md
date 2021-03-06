# HTML

[HTML Cheatsheet](https://htmlcheatsheet.com/) alot of good examples.

**HyperText Markup Language**

We use HTML to give structure to our webpages, you can see them as building blocks.

## Basic structure

```HTML
<!DOCTYPE html>
  <html lang="en">
    <head>
      <title>Page Title</title>
      <style>
        img {

        }
      </style>
    </head>
    <body>
      <h1>My First Heading</h1>
      <p>My first paragraph.</p>
      <img src="" alt="">
  </body>
</html>
```
> Get HTML boilerplate code by typing '! & tab' in visual studio

`<head>` = Browser information

`<body>` = Elements that will appear on our page

`<image src="" alt="">` = Element has attributes, with these attributes we can supply additional information about an element.


## Basic CSS Styling

Adding basic styling in the header section. Using a `<style></style>` block

```HTML
<style>
  img {
    width: 100px;
    height: 100px;
  }
</style>
```

## Validating HTML
[Validator w3 org](https://www.validator.w3.org "HTML Validator")

This will validate your HTML code and make remarks on things that need to be added. (ex. missing alt attribute on an image).

## Validating CSS
[Validator CSS org](https://jigsaw.w3.org/css-validator/ "CSS Validator")


## Essential HTML elements

### Head Section
All the elements in the headsection give information about the webpage.

`<meta charset="UTF-8">` 

= defining the character set. The character set let's us map a letter to a numerical value. (ex. ASCII, ...)

`<meta name="viewport" content="width=device-width, initial-scale=1.0">` 

= Defines the inital width and zoom factor for the viewport. This makes the website look good on all devices.

type `meta` in the header section to find all other properties which can be configured.

### Text
`<h1>Title</h1>` 

= Headings 1 > 6 gives importance to the header. 1 being the most important to 6 being the least important. It is used for creating hierarchy. There should only be 1 h1 element per page.

`<p>Test Text..</p>` 

= Gives a text block/paragraph

`<em></em>` 

= Emphasis content. In default it puts text in italic. It's usually used in between `<p>`tags. It is strongly discouraged to use inline styling such as `<Strong>`, `<i>` etc...

### Entities
Special characters that don't get recognized without special syntax. 

`&copy;` = &copy;

`&lt;` = &lt;

### Links
`<a href=""></a>`

`<a href="company/about.html"></a>`

`<a href="images/mosh.jpg" download></a>`

= Known as anchor tags, let's you add links to the href section

`<a href="#section-id"></a>`

`<a href="#"></a>`

`<a href="https://google.com" target="_blank"></a>`

`<a href="mailto:jens.bols@hotmail.com"></a>`

= adding an id to an element and referencing it in an anchor tag like above will make it a link to a place in a page. 

Using `#` creates a link to the top of the page.

Using `target="_blank"` opens the link in a new tab.

### Images

Best practice to use discriptive image names.

`<image src="" alt="">`

It is important to give a good alternative text, this is for visually impaired users.

Styling should be added in css classes.

> `object-fit: cover` is usefull for making images fit

### Lists & Tables
#### Tables
```HTML
<table>
  <tr>
    <th>Company</th>
    <th>Contact</th>
    <th>Country</th>
  </tr>
  <tr>
    <td>Alfreds Futterkiste</td>
    <td>Maria Anders</td>
    <td>Germany</td>
  </tr>
  <tr>
    <td>Centro comercial Moctezuma</td>
    <td>Francisco Chang</td>
    <td>Mexico</td>
  </tr>
</table>
```

#### Lists
```HTML
UnOrdered List
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>

Ordered List
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

### Container elements

`<div></div>`

A container for a block of content.

`<span></span>`

A container for in-line content, such as content inside a paragraph.
### Structural elements | Semantic Elements

A semantic or structural element describes its meaning to both the browser and the developer.

Examples of **non-semantic** elements: `<div> & <span>`
Examples of **semantic** elements: `<form>, <table>, <article>, <nav>,..`

![Semantic Elements](/images/HTML/semanticElements.png)

`<section>`

Defines a section in a document. It's a thematic grouping of content, typically with a heading.

ex. Chapters, Introduction, News Items, Contact information.

`<article>`

Specifies independent, self-contained content. An article should make sense on its own, and it should be possible to distribute it independently from the rest of the website.

ex. Forum posts, Blog posts, User comments, Product cards, Newspaper articles


## Forms and Validations

```HTML
<form action="results.html" method="GET">
  <div>
    <label>Name</label>
    <input>
  </div>
  <div>
    <label>Password<label>
    <input>
  </div>
  <button type="submit">Submit</button>
</form>
```

All inputs between `<form></form>` will be submited to wherever you send your form. By default if you leave it blank it will submit it to the page you are currently on.

We need a way to submit the form so you always need a button. To set a location to send the form you need to add an `<form action="">`attribute.

By adding a method to the form you are specifying wether you want to append things to the url and send it to another page on your site by using a `method="GET"` method. `method="POST"` will be usefull if you have a server and want to save information.

If you don't add a `name="name"` label to inputs there is no way of knowing what information is what.

You will also see those parameters in the URL when using a GET request.

You should add `for="inputId"` labels in label elements. this helps screenreaders and users. Also add an ID to the input field `id="inputId"`.

An alternative to using Ids, you can wrap the input field with `<label>` tag.

### Input types

It is important that you specify the type of the input data. You should also match input fields by using an id reffering to the label.

`<input type="text" value="defaultValue" placeholder="username" required>`

`<input type="email">` basic email validation and gives different keyboard for mobile phones. 

`<input type="password" required>` hides the characters

`<button type="submit">` submit the form by using enter or clicking the button. 

`<button type="reset">` reset the form to default.

`<input type="number" name="age" id="age" min="1" max="200" step="1">` jump numbers by step

`<input type="date" name="date" id="date" min="2019-06-10">`

`<input type="checkbox" name="banana" id="banana">` allows multiple checkboxes to be checked

`<input type="radio" name="gender" id="male" value="male">` share the same name to get a grouped radio button

`<input type="radio" value="female ...">` the value property makes it so when the form gets sent the format will be `gender: value`

```HTML
<select name="eyeColor" id="eyeColor" multiple>
  <option value="Green">Green</option>
  <option label="Red" value="Red"></option>
</select>
```
Multiple flag allows to select multiple options using control+click.

`<textarea id="bio"></textarea>` add default value between tags.

`<input type="hidden" name="hidden" value="hi">` allows hidden input the user can't see

`<input type="file" ...>` 

add `enctype="multipart/form-data"` to the `<form>`tag. files can be large so adding this argument sends the form in multiple packets.

`<input type="tel" ...>` on phone will give special numpad

`<input type="url" ...>`

`<input type="color" ...>`


## Best Practices

[Best Practices](https://github.com/hail2u/html-best-practices)













