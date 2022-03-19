# Javascript

## Dom Manipulation

`const body = document.body` when you have the body it's easy to append items to it.

`body.append("hello world", "")` with append you can append strings with `body.appendChild()` you can append divs, spans etc..

### Creating elements

`const div = document.createElement('div')`

### Modifying element text 

`div.innerText = "hello world"`

`div.textContent = "hello world 2"` is the content straight from the html, if you write text on 2 lines it will be like that in the textContent.

the difference between `innerText` and `textContent` is that when you put something on `display:none` the `textcontent` is not empty. While with `innerText` it is gone.

`body.append(div)`

### Modifying HTML element

`div.innerHTML = <p>tekst<p>` allows html elements to be added. if you allow user input into innerHTML they could write malicious code.

`const item = document.querySelector('#id')` allows getting items

`item.remove()` removes the item from html

### Modifying element attributes

`item.getAttribute('id')` not used that much, can be handy when the property is unknown at that time.

`item.id` is easier way

`item.setAttribute("id","123")`

`item.id = 123` 

### Modifying data attributes

`<p data-test-name="anything">`

`item.dataset.testName` get or set

### Modifying element  classes

`item.classList.add("new-class")`

`item.classList.remove("new-class")`

`item.classList.toggle("class", ?bool)` most common way to use classList

### Modifying element styles

`item.style.color = "red"`


## Learn Fetch API

```JS
fetch('https://localhost:3000/api/list')
  .then(res => {
    console.log('Success');
  })
  .catch(err => {
    console.log('failed');
  })
```

fetch returns a promise, `res` is the result. still gives succes even when you send faulty request.

add `console.log(res.ok, res.status)` allows to see the actual response

you can chain promises:

```JS
fetch('...')
  .then(res = {return res.json()})
  .then(post => {console.log(post)})
```

add parameters in url: `('url/api/post/?var1=123&?var2=123)`

![Fetch API](../images/Javascript/fetchapi.PNG)

```JS
// Example POST method implementation:
async function postData(url = '', data = {}) {
  // Default options are marked with *
  const response = await fetch(url, {
    method: 'POST', // *GET, POST, PUT, DELETE, etc.
    mode: 'cors', // no-cors, *cors, same-origin
    cache: 'no-cache', // *default, no-cache, reload, force-cache, only-if-cached
    credentials: 'same-origin', // include, *same-origin, omit
    headers: {
      'Content-Type': 'application/json'
      // 'Content-Type': 'application/x-www-form-urlencoded',
    },
    redirect: 'follow', // manual, *follow, error
    referrerPolicy: 'no-referrer', // no-referrer, *no-referrer-when-downgrade, origin, origin-when-cross-origin, same-origin, strict-origin, strict-origin-when-cross-origin, unsafe-url
    body: JSON.stringify(data) // body data type must match "Content-Type" header
  });
  return response.json(); // parses JSON response into native JavaScript objects
}

postData('https://example.com/answer', { answer: 42 })
  .then(data => {
    console.log(data); // JSON data parsed by `data.json()` call
  });
```
---

## ES6+ and modular Javascript

### Template Literals

allow us to use javascript between backticks `${var1} ${num1 + num2}`


https://www.youtube.com/watch?v=nZ1DMMsyVyI&ab_channel=freeCodeCamp.org 4:18