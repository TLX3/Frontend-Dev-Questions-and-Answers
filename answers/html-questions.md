# HTML Questions

#### What does a `doctype` do?
doctype declaration is an instruction to the web browser about what version of the markup language the page is written in. doctype ensures that the browser renders the page in standards mode instead of quirks mode.
#### What's the difference between standards mode and quirks mode?
quirks mode provides compatibility with older web browsers by handling rendering idiosyncratically.
#### What's the difference between HTML and XHTML?
XHTML is HTML that follows the rules of XML.
#### Are there any problems with serving pages as `application/xhtml+xml`?
Lack of older browser support and XHTML must be well formed.
#### How do you serve a page with content in multiple languages?
Set the language attribute on the html tag to declare the default language. For a language that differs from the default, set the lang attribute on the element surrounding it.
#### What kind of things must you be wary of when design or developing for multilingual sites?
How will users be directed to their native language? You can either design an UI that allows users to change it or redirect the browser based on the user's IP. Will each language have its own URL or domain?
Text in images won't scale.
Cultural differences in color.
Remove text content from templates
Date formatting
#### What are `data-` attributes good for?
It lets you assign custom data to an element. You can easily associate some scripting data with your elements without having to insert inline javascript.
#### Consider HTML5 as an open web platform. What are the building blocks of HTML5?
HTML5 is the latest version of HTML. It consists of new semantic tags, new form elements, video and audio, canvas, SVG, javascript API, communication API, geolocation API, web worker API, and new data storage.
#### Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
All three are used to store data on the client side. Each has its own storage and expiration limit. localStorage stores data with no expiration data and gets cleared only through JS, or clearing the browser cache. sessionStorage is similar to localStorage but expires when the browser closes. Cookies stores data that has to be sent back to the server with subsequent requests.
#### Describe the difference between `<script>`, `<script async>` and `<script defer>`.
`<script>` is the default behavior and parsing of the HTML code stops while the script is executing. This might delay the display of the webpage.
`<script defer>` delays script execution until the HTML parser has finished parsing. The DOM will be ready for this script but not all browser support defer yet.
`<script async>` allows HTML parsing to continue also the script to be executed when ready.
#### Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
The link tag placement allows for styles to be loaded beforehand so that users don't see a blank screen. The script tag placement ensures that the HTML parser isn't blocked until the very end. An alternative is to use the async or defer attributes on script tags.
#### What is progressive rendering?
It is a technique used to render content as quickly as possible.
#### Have you used different HTML templating languages before?
ERB
