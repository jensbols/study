# Javascript

## Dom Manipulation

`const body = document.body` when you have the body it's easy to append items to it.

`body.append("hello world", "")` with append you can append strings with `body.appendChild()` you can append divs, spans etc..

`const div = document.createElement('div')`

`div.innerText = "hello world"`

`div.textContent = "hello world 2"` basically is the content straight from the html, if you write text on 2 lines it will be like that in the textContent.

the difference between `innerText` and `textContent` is that when you put something on `display:none` the `textcontent` is not empty. While with `innerText` it is gone.

`body.append(div)`



