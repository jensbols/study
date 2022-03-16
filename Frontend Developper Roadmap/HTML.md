# HTML

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

`<a href=" company/about.html"></a>`

`<a href="images/mosh.jpg" download></a>`

= Known as anchor tags, let's you add links to the href section

### Images
### Lists & Tables
### container elements
### Structural elements

