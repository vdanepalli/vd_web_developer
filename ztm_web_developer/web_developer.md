# Web Developer

- [Web Developer](#web-developer)
  - [How the Internet Works](#how-the-internet-works)
    - [Browsing the web](#browsing-the-web)
  - [History of Web](#history-of-web)
  - [HTML5](#html5)
  - [CSS](#css)
  - [Bootstrap, Templates](#bootstrap-templates)
  - [CSS Grid, CSS Layout](#css-grid-css-layout)
  - [Career of a Web Developer](#career-of-a-web-developer)
  - [JavaScript](#javascript)
  - [DOM Manipulation](#dom-manipulation)
  - [Advanced JavaScript](#advanced-javascript)
  - [Command Line, Developer Environment](#command-line-developer-environment)
  - [Git, GitHub, Open Source Projects](#git-github-open-source-projects)
  - [NPM, NPM Scripts](#npm-npm-scripts)
  - [ReactJS Fundamentals](#reactjs-fundamentals)
  - [React Hooks](#react-hooks)
  - [Asynchronous JavaScript](#asynchronous-javascript)
  - [Backend, APIs](#backend-apis)
  - [Final Project: Smart Brain Front End](#final-project-smart-brain-front-end)
  - [NodeJS, ExpressJS](#nodejs-expressjs)
  - [Final Project: Smart Brain Backend Server](#final-project-smart-brain-backend-server)
  - [Database](#database)
  - [Final Project: Smart Brain Backend Database](#final-project-smart-brain-backend-database)
  - [Production Deployment](#production-deployment)
  - [Other](#other)
  - [Conclusion](#conclusion)


## How the Internet Works

### Browsing the web 

- Browser --(google.com)--> ISP ----> DNS --(IP address)--> Browser 
- Browser ----> Google Servers --(html, css, js)--> Browser
- [Command Line](https://www.lifewire.com/how-to-open-command-prompt-2618089)
- [Windows Terminal](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701)
- `traceroute -4 google.com` -4 to force to ipv4 instead of ipv6; mac
- `tracert google.com` -- widnows
- BASH - Bourne Again Shell
- speed
  - location of servers
  - how many trips between server and browser
  - size of files 

## History of Web

- Tim Berners Lee -- Invented World Wide Web (WWW) in 1989 -- say a common language; agreed protocols
- WWW, HTML, CSS, JavaScript | HTML, CSS, JavaScript, React 
- JQuery is a library -- makes writing JavaScript easy, clean, simple way; An environment for JS | React
- Backend LAMP Stack
  - Linux
  - Apache Server -- HostGater, ... | Node Server
  - MySQL | PostgreSQL, MongoDB
  - PHP | Node.JS Express.JS

## HTML5

- HyperText Markup Language
- `<!DOCTYPE html> <html> <head> <title></title></head>  <body></body></html>`
- `h1, h2, h3, h4, h5, h6` -- big to small -- headers
- `p` -- paragraphs
- `b` -- `strong`
- `i` -- `em`
- `<ol> <li></li> <li></li></ol>` | `<ul> <li></li> <li></li></ul>`
- `<img src="" alt="" width="" hegiht="">`
- `<br>`
- `<a href=""></a>`

```html
<form method="GET" action="run_script_on_server.php">
		First Name: <input type="text" name="firstname"><br>
		Last Name: <input type="text" name="lasttname"><br>
		Email: <input type="email" name="email"><br>
		Password: <input type="password" name="password" minLength="5"><br>
		Birthday: <input type="date" name="birthday"><br>
		Gender:<br>
		<input type="radio" name="gender" value="Male">Male<br>
		<input type="radio" name="gender" value="Female">Female<br>
		<input type="radio" name="gender" value="Other">Other<br>
		Pets: <br>
		<input type="checkbox" name="cat"> Cat<br>
		<input type="checkbox" name="dog"> Dog<br>
		Cars: <br>
		<select name="cars">
			<option value="volvo" >Volvo</option>
			<option value="audi">Audi</option>
		</select><br>
		<input type="submit" value="Register!">
		<input type="reset">
	</form>
```

- query strings/parameters --- index.html?name1=val1&name2=val2&name3=val3...
  - when you use form GET method -- you can see this in URL
  - when you use form POST method -- these are attached to the body request
- comments `<!-- sometext -->
- `<div></div>` -- block element
- `<span></span>` -- inline element
- semantic elements in Html5
  - `<header></header>`
  - `<nav></nav>`
  - `<footer></footer>`
  - `<section></section>`

## CSS

- Cascading Style Sheets
  - always takes the selector at the end
- comments `/* .... */`
- `Selector {Property : Value;}` 
- `<link rel = "stylesheet" type="text/css" href="___.css">`
- `<tag style="background-color: green; color:red;></tag>` -- inline styles
- `<head> <style> .... </style></head>`
- `rgb(red, greeb, blue)` 0 - 255
- `rgba(red, green, blue, alpha)` 0 - transparent; 1 - opaque

```css
body{
    background-image : url(path.jpg);
    background-size : cover; 
}

h2{
    color: #FF0000;
    text-align: center;
    border: 5px dashed/solid rgba(....);
    cursor: pointer;
}

li{
    line-style: none; /* removes the . from li in ul */
    display: inline-block/block; /* inline-block is horizontal; block is vertical -- default */
}
```

- class -- select a group of elements and css selector is `.class{ .... css ...}`
  - `<p class = "webtext active"></p>` -- webtext is one class, active is another class. same element can have multiple classes
- id -- you can use only once for one element  and css selector is `#id{ .... css ...}`
- `*{ text-align: right;}` -- selects everything
- element
- element1, element2 -- all element 1s and all element2s
- element1 element2 -- all element2s inside element1s
- element1 > element2 -- all element2s where their parent is element1
- element1 + element2 -- select any element2 that is right after element1
- selector:hover
- selector:last-child
- selector:first-child
- property:value !important; -- this won't be overwridden by next coming css



<br/><br/>

- Specificity -- how specific are your selectors 
  - Inline Syles > Ids > Classes, Attributes, Psuedo-Classes > Elements and Psuedo Elements
- Importance !important
- Source Order -- when there are multiple stylesheets linked


<br/><br/>

- text-decoration: underline | line-through
- text-transform: uppercase 
- line-height: 20px;
- font-style: italic;
- font-weight: bold; you can also do a number between 100 and 900
- font-size: 100%; 
- font-family: "Times New Roman", Georgia;  -- falls back to Georgia if TNR is not available


<br/><br/>

- `img {float: left | right}` -- wraps text around image 
- `footer{ clear: both; text-align: center}` -- this needs to always added after above 


<br/><br/>

- Box Model
  - Margin > Border > Padding > Content
```css
.boxmodel{
    border: 5px solid red;
    display: inline-block;
    padding: 5px 20px 5px 20px; /* top right bottom left */
    margin: 0px 20px; /* top and bottom, left and right */
    width: 39px; /* content */
    height: 12px; /* content */
}
```

- px, em, rem
  - px 
  - em -- size in relation to parent element size;  so say `2em` -- twice the size of the containing element
  - rem -- size in relation to the size of the root element;


<br/><br/>

- Critical Render Path
  - Fetch HTML and start reading
  - Fetch CSS and Fonts (render blocking; html file can't render without these)
    - So minifying css might help reduce the number of bytes transferred over wire
  - Reder
- Flexbox
  ```css
  .container{
    display: flex; /* activate flexbox */
    flex-wrap: wrap; /* doesn't put all in one line; */
    justify-content: center;  
  }

  h1{
    border-bottom: 5px solid pink;
    border-rigth: 2px solid red;
    width: 400px;
    font-family:fantasy;
    font-size: 3em;
    text-align: center;
  }
  ```


```css

img {
    width: 339px;
    height: 312px;
    margin: 12px;
    transition: all 1s; /* transition when action is taken upon this is 1s */
}

img: hover{
    transform: scale(1.1); /* specifies the transformation */
    animation: ... 
}
```

- `border-radius: 1px 10px 20px 30px;` -- top left, top right, bottom right, bottom left;

## Bootstrap, Templates

- CSS file and JS file
  - use something that is already created by someone
- CDN : Content Delivery Network
  - some place that is actually hosting the file
- Put you JS at the bottom of the body so that you load these after all content is loaded. Otherwise you will have to wait until all JS is loaded to load the content


<br/><br/>

- Bootstrap Grid (think as 12 spaces for a row)
```html
<div class="container">
  <div class="row">
      <div class="col col-sm-6 col-md-12 col-lg-12"> Col1 </div>
      <div class="col col-sm-3 col-md-6 col-lg-12"> Col2 </div>
      <div class="col col-sm-3 col-md-6 col-lg-12"> Col3 </div>
      <!-- all 3 cols add up to 12 for small -->
      <!-- 12 on its own and 6 and 6 for the next row for medium -->
      <!-- everything on its own -- 12 for each -->
</div>
```

- `meta` allows us to add new information to the page; 
  - responsive meta tag `<meta name="viewport" content="widht=device-width, initial-scale=1, shrink_to_fit=no">`
  - meta charset="utf-8"
- `container d-flex justify-content-center align-items-center h-100` 
  - container, h-100 are bootstrap classes
  - d-flex activates flex features
  - align-items-center -- aligns to center; flex feature
  - justify-content-center -- without this, h1 with shorter text might not align to center of the browser's window; Rather it makes max width  the total width of h1 or button (which ever is longer), aligns left, then centers
- Email Marketing Service
  - Mailchimp
    - Free up to 2000 contacts
  - MailerLite
  - ...
- 


## CSS Grid, CSS Layout


## Career of a Web Developer


## JavaScript 



## DOM Manipulation


## Advanced JavaScript


## Command Line, Developer Environment



## Git, GitHub, Open Source Projects


## NPM, NPM Scripts


## ReactJS Fundamentals


## React Hooks


## Asynchronous JavaScript


## Backend, APIs


## Final Project: Smart Brain Front End


## NodeJS, ExpressJS


## Final Project: Smart Brain Backend Server


## Database


## Final Project: Smart Brain Backend Database


## Production Deployment


## Other



## Conclusion