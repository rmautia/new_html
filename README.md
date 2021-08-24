# Front End Development (Day 1 of 2)
--- 
# HTML
     Hypertext Markup Language
- Not a Programming Language
- Used to build structure of website

# CSS
     Cascading Style Sheet Language
- Not a programming language
- Used to style website

# JavaScript
     Programming language, add interactivity.

## Objective :
---
1. Basic idea about how websites are built
2. Understand common html tags
3. Understand common html attributes
4. Understand HTML DOM Hierachy
5. Build simple structure with common html elemnts
6. Add simple styling with common css
7. Understand how CSS target elements to add styles
8. Extreme basic javascript
9. Understand how javascript identify elements to add interactivity

--- 
### Let’s create our first HTML file
1. Create a new folder on your Desktop called: `HTML_Class`
2. Drag and drop into **Sublime Text**
3. Create a new file inside of the `HTML_Class` folder
    1. `File` > `New File`
4. Give it a name `myFirstPage.html`
5. `File` -> `Save as` > Select Desktop > Select `HTML_Class` folder and save
6. Navigate to the folder on your desktop and open it with Google Chrome
    - you can double click to open and it will open on default browser you have)
7. Now it's time to edit the html file in sublime
    1. Html use this syntax to represent elements on the web
   ```html
    <tagName> content </tagName>
   ```
    2. in your empty html file , type `html` and hit `tab` key on your keyborad and it will generate below skeleton for you
   ```html
     <!DOCTYPE html>
     <html>
     <head>
          <meta charset="utf-8">
          <title></title>
     </head>
     <body>

     </body>
     </html>
   ```
8. Type `Cool Website` in between `title` tag in line 5
   ```html
     <title>Cool Website</title>
   ```
9.  Save it and open again in chrome(refresh) to observe the page title in browser tab has changed to `Cool Website`
10. Now inside `body` tag line number 8 enter below heading
     ```html
     <h1>this is my first h1 tag</h1>
     ```
11. Save the file and refresh chrome to see the change .
12. and continue to add more
---
# Working with HTML in IntelliJ
IntelliJ has strong support for creating and editing html file and support all emment shortcuts to easily generate html elements.

You can create a new HTML file literally in any existing project you have and directly see your result inside IntelliJ Preview or browser

If you want to import the folder you created earlier simply do below
1. From top menu `File`->`Open`->Select `Desktop`-> Select `HTML_Class` folder
2. Click open (do not select file, select **HTML_Class Folder**)
3. Now you will see your html file and can edit directly in familiar IntelliJ environment
4. In order to visually see structure of your html file you can go to top menu
5. `Views` -> `Tools Windows` -> `Structure`
    1. Shortcut for mac `Command + 7`
    2. Shortcut for win `Alt + 7`
6. IntelliJ or other tools has HTML CSS shortcut tools known as `Emmet` to make your html less error prone by auto-generating most of the tags and attribute typing for examle :
    1. `h1` + tab -> `<h1></h1>`
    2. `p*2` + tab ->
        - `<p></p>`
        - `<p></p>`
    3. `ul>li*3` + tab
   ```html
     <ul>
          <li></li>
          <li></li>
          <li></li>
     </ul>
   ```
    4. and many more here is [the full cheatsheet](https://docs.emmet.io/cheat-sheet/)

---
Here is the full [list of html tags](https://www.w3schools.com/tags/default.asp).  
We will not go through all of them we will see some of the most common ones in the majority of websites.
## Heading  `h1-h6`
```html
<h1> This is h1 heading content </h1>
<h2> This is h2 heading content</h2>
<h3> This is h3 heading content </h3>
<h4> This is h4 heading content</h4>
<h5> This is h5 heading content </h5>
<h6> This is h6 heading content</h6>
```

## Commenting in HTML
```html
<!--  Anything inside here is comment -->

<!-- <h6> Command + / or Control +/ for comment </h6> -->
```

## Paragraph `<p>` tag
```html
<p> content goes here </p>
```
You can easily generate dummy text by typing `lorem` and hitting tab. you can also specify how many word you want by `lorem10` -> 10 words.

### Quick Task
1. Add one `H1` heading
2. Add 3 paragraphs with `p` tag
3. Add another `H2` heading
4. Add 2 paragrapth with `p` tag

## Breaking up lines `<br/>` , `<hr/>`
```html
<p> Lorem ipsum  <hr/> dolor sit amet, consectetur adipisicing elit, sed do eiusmod </p>
<hr/>
```
these two tags are for breaking up text or elements from the middle because html will ignore any white space more than 1.


## Making text bold `<strong>`
```html
<p>This is very <strong> important </strong>  topic</p>
```
The text important will be bolded

## Making text italic `<em>`
```html
<p>This is <em> cool </em>  topic</p>
```
The text cool will be italic

## Making text underline `<u>`
```html
<p>This is <u> underlined </u>  text</p>
```
The text `underlined` will be itaunderlinedlic


## `Element` **`Attributes`**
We can provide key value pair inside opening tag to provide more information about the elememt to transform the elements look or style and others.
```html
<p lang="en-us">  This is an english text I added attribute called lang into this element   </p>
<p style="color: red" >  THIS TEXT SUPPOSED TO BE RED  </p>
```
in above example `lang` and `style` are attribute name `en-us` and `color: red` are attribute value. one element can have many attributes.

## Adding link using `<a>` tag
You can add link to a destination by providing `href` attribute , it can point to a external url or other html files in the project. if `target` attribute is not set to `_blank` it will open the link in same tab.

1. external link , open in same tab
```html
<a href="https://www.google.com">Google home page</a>
```
2. external link , open in new tab
```html
<a href="https://www.cybertekschool.com/" target="_blank"> Link to Cybertek HomePage  </a>
```
3. link to other html file , below example will be linked to a html file called `about.html` in same directory
```html
<a href="about.html" target="_blank"> About Me </a> 
```


## Adding Image : `<img>` tag
img tag is a self closing tag, It is used to display images using the attribute `src` to specify either local destination or remote url destination
Assuming that you have picture in same directory(folder) with the name `TheCoolPic.jpg`. Here is how you can display it as element
```html
<img src="TheCoolPic.jpg"> 
```
Common attribute for `img` tag is `alt` to provide description about the image and also `height` and `width` attributes can be used to adjust the size (even thout it's recommended to do it with css)
```html
<img src="TheCoolPic.jpg" height="500"  alt="The mandalorian picture" />
```
If you have picture in different location on your computer, you can still provide full path to display it in your html page as below
```html
<img src="Full/Path/To/Image/Folder/TheCoolPic.jpg" height="500"  alt="The mandalorian picture" />
```
You can also display image in remote location by providing it's url as below example
```html
<img src="https://www.cybertekschool.com/wp-content/uploads/2020/04/bycer-1.png" height="100" alt="cybertek campus">
```

## Block | Container `<div>`
The `<div>` HTML element is the generic container for flow content. It has no effect on the content or layout until styled in some way using CSS.

We just had 3 images in above example , if we add last 2 images to into div element it will treat it as a block and will show up in new line rather than putting 3 picture side by side.
```html
<img src="TheCoolPic.jpg" alt="mandalorian1"> 
<div>
     <img src="TheCoolPic.jpg" alt="mandalorian2">
     <img src="TheCoolPic.jpg"alt="mandalorian3">
</div>
```
This is just a quick example , it will become much more obvious when it is combined with css later.

## HTML List
* Ordered List (1.2.3.)
    - short cut to generate one ordered list with 3 items `ol>li{item$$}*3`
  ```html
     <ol>
          <li>Item01</li>
          <li>Item02</li>
          <li>Item03</li>
     </ol>
  ```
    1. Item01
    2. Item02
    3. Item03
* Unordered List (* * * *)
    - short cut to generate one ordered list with 3 items `ul>li{item$$}*3`
  ```html
     <ul>
          <li>Item01</li>
          <li>Item02</li>
          <li>Item03</li>
     </ul>
  ```
    - Item01
    - Item02
    - Item03

## HTML `<table>`
- `<table>` tag is to define table
- `<thead>` tag to define this is where header go
- `<tr>` to define this is table row
- `<th>` to define this is actual table header
- `<td>` to define cell value
- `<tbody>` to define table body other than header
- `<tr>` table rows
- `<td>` actual cell

Emmet shortcut to generate below table
`table>thead>(tr>td{Header$}*2)^tbody>tr*3>td{Value$$$}*3**`

  ```html
      <table>
        <thead>
              <tr>
                   <td>Header1</td>
                   <td>Header2</td>
              </tr>
        </thead>
        <tbody>
              <tr>
                   <td>value001</td>
                   <td>value002</td>
              </tr>
              <tr>
                   <td>value001</td>
                   <td>value002</td>
              </tr>
              <tr>
                   <td>value001</td>
                   <td>value002</td>
              </tr>
        </tbody>
    </table>
  ```  
