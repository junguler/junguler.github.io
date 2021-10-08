this will eventually become my personal website, little progress have been made already toworeds that goal but i suspect it's going to be a long process but one thing i have is patience so it's fine by me.

#### what i've learned so far:
- [x] add website title 

set the page title`<title>junguler</title>` 

- [x] set icon on tab bar

set page icon in the tab bar `<link rel="icon" type="image/ico" href="stuff/favicon.ico"/>` here i've uploaded `favicon.ico` to the stuff folder of this repo, head over [this site](https://iconifier.net/) to convert your image to favicon

- [x] upload a picture to repo and link it 

upload your image to a folder in the repo, `stuff` in this case and link it `<img src="stuff/avatar.jpg"/>`

- [x] center everything in the page

start centering with `<center>` at the beeging and end it with on the last few lines `</center>`

- [x] link some sites

link a wbsite like this `<a href="https://www.deviantart.com/junguler">deviant art page</a>` the first part is the actual link, the second part is what people see on your site

- [x] have a link to email me with emails clients

same as above, the first part is the actual email, the second part is what people see`<a href = "mailto: junguler@yahoo.com">email: junguler@yahoo.com</a>`

- [X] apply a border around the page
- [X] change background color to black and text to white
- [X] apply margin spacing to left and right of the page

```
<div style="background-color:black;color:white;padding:50px;margin:0px 150px 0px 150px;border-style: solid; border-width:5px;border-color: white;">
```
specify background and text colors `background-color:black;color:white` specify the distance each element will have to each outher `padding:50px` specify border margin (un-available area in the page) the order is top, right, bottom, left `margin:0px 150px 0px 150px` specify the border width and color `border-width:5px;border-color` the whole line is covered in double quates `""` and each part is seperated by `;`

use `<h1>header</h1>` for header text, for writing prographs start with `<p>` and end with `</p>`, use `<br>` for line breaks and put everything in `<body>everything</body>`

- [X] change font size

use the font tag `<font size="5"> <p>your size 5 paragraoh</p> </font>` more examples can be found [here](https://www.tutorialspoint.com/html/html_fonts.htm)

- [X] change link colors

`<a href="web link" style="color:yellow">what people see on the site</a>` or use `#FF0` or `#ffff00` for the same yellow color, use `background-color:#666` to set background color

- [X] make a button for links
```
  <br> <form action="page link">
      <input type="submit" value="writings on the button"> 
  </form> <br>
```
- [X] add a download link in your site
```
<a href="link of file to download">what people see on the site/a> <br>
```
- [X] add an image and link a page to it
```
<br> <a href="page link"><img src="image.jpg png or something else" width="48" height="48" alt="optional name"></a>
```
- [X] create extra page(s), link it/them to main page and vise versa

this process is split between two, first we make a pages folder and put second.html in it, inside it we link to the main index.html
```
<a href='../index.html'> go to main page </a>
```
`../index.html` tells the page to go up/back one folder, now add the link of the second page to the main index.html
```
<a href='pages/second.html'> second page of my website </a>
```
- [X] apply styles to a tag by including them inside < >

```
<b style="font-size: 24px">_image-manipulation:</b> 
```
change font size with bold text, styles can be `color`, `background-color`, `font-family`, `font-size`, `text-align` and more, for more information go [here](https://www.w3schools.com/html/html_styles.asp)

- [X] linking to different folders of the website relatevly

for example linking to the page favicon becomes `../stuff/favicon.ico` instead of `stuff/favicon.ico` in the main index.html, because in the `second.html` page we are in the `pages` folder and need to go back a folder `../` and then go to the `stuff` folder to link the favicon. for more info check this [stackoverflow](https://stackoverflow.com/questions/908765/how-to-link-html-pages-in-same-or-different-folders) page for more examples

- [X] add pictures and thumbnails to second/project page

lets start by making a second folder named `secondpage` in our `stuff` folder, copy you images and lets make thumbnails for them:
```
ffmpeg -i g_1.jpg -vf scale=-1:140 t-g_1.jpg
```
here we import the image with `-i g-1.jpg` apply scale filter to it, note we want to have unfied height for our thumbnails so we let ffmpeg decide their width by `-vf scale=-1` the only part we care about is height that we set to 140 pixels and lets add a `t-` behind the names to be able to easiliy differentiate them

now make a thumbnail and link the image, again we have to link relatevly to the whole folder sctructure of our website
```
<a href="../stuff/secondpage/gm_1.jpg"><img src="../stuff/secondpage/t-gm_1.jpg" alt="optional name"></a>
```
throw a couple of `<br>` on there which are break tags so everything is not stuck toghetere
```
<br> <a href="../stuff/secondpage/gm_1.jpg"><img src="../stuff/secondpage/t-gm_1.jpg" alt="optional name"></a> <br><br>
```

#### what i'm planning to do in the near future:
- [ ] add icons for each page and link the websites to the icons
- [ ] add picture examples for each project in the second/project page
- [ ] add bling, pictures, animated gifs, videos
- [ ] change fonts for everything, add a [nerd font](https://github.com/ryanoasis/nerd-fonts) to this repo and use it's glyphs
- [ ] replace the basic avatar with animated picture, preferably with fake 3d effect from G'mic
- [ ] add different sub-pages whitin the site
- [ ] learn some basic css to make life easier
- [ ] and ...
