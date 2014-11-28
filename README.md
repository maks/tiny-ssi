# tiny-ssi

A minimal implementation of Apache SSI (server-side includes)


## Usage

Currently only reall supports doing includes, eg. 

```html

 <!--#include virtual="header.html" -->
 
    <div class="container">
        <h1>title</h1>
        <p class="lead">
          contents
        </p>
    </div>
 <!--#include virtual="footer.html" -->

```

expecting that 'header.html' and 'footer.html' are in the same folder as the above html file,
you can then do:

```javascript
var ssiParser = require('tiny-ssi');

var finalHTML = ssiParser("/dummy/path", someHTMLContent); 
console.log("processed html looks like:"+finalHTML);
```

## License

MIT

