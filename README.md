my work in progress website, the old markdown file was moved to [old-README.md](https://github.com/junguler/junguler.github.io/blob/main/old-README.md) for archivable purposes and i try to explain what i've learned better this time

### quick links
 * [first step](https://github.com/junguler/junguler.github.io#first-step)
 * [make index.html](https://github.com/junguler/junguler.github.io#make-indexhtml)
 * [vscodium](https://github.com/junguler/junguler.github.io#install-vscodium-or-another-ide)
 * [some basic tags](https://github.com/junguler/junguler.github.io#some-basic-tags-and-how-to-use-them)
 * [add files to repo](https://github.com/junguler/junguler.github.io#add-files-to-your-repo)
 * [link files in the webpage](https://github.com/junguler/junguler.github.io#link-a-file-that-you-uploaded-in-the-directory-in-your-page)
 * [add favicon](https://github.com/junguler/junguler.github.io#add-favicon-to-your-page)
 * [add styles to tags](https://github.com/junguler/junguler.github.io#add-styles-to-tags)
 * [add padding to page](https://github.com/junguler/junguler.github.io#add-padding-to-our-page)
 * [add extra pages](https://github.com/junguler/junguler.github.io#add-extra-pages-to-our-site)
 * [link extra page to home](https://github.com/junguler/junguler.github.io#link-the-second-page-to-our-homepage-and-vise-versa)
 * [add footer to pages](https://github.com/junguler/junguler.github.io#add-footer-to-our-pages)
 * [add white spaces](https://github.com/junguler/junguler.github.io#add-white-space-in-html)
 * [align text to left and image to right](https://github.com/junguler/junguler.github.io#align-text-to-left-and-image-to-the-right)
 * [force content to stay in the page when zoomed in](https://github.com/junguler/junguler.github.io#keep-banner-from-overflowing-the-page)
 * [add go to top button](https://github.com/junguler/junguler.github.io#add-go-to-top-button)
 * [add background image or use gradient colors](https://github.com/junguler/junguler.github.io#change-background-color-or-use-an-image)
 * [add some basic css](https://github.com/junguler/junguler.github.io#add-some-basic-css)
 * [write in markdown and convert it to html](https://github.com/junguler/junguler.github.io#write-in-markdown-and-convert-to-html)
 * [embed video in your page](https://github.com/junguler/junguler.github.io#embed-video-in-your-page)

### first step
make a github account, start a new repo with your username and add `.github.io` at the end of it, see [here](https://pages.github.com/) for detailed information

### make index.html
make a new file named `index.html` this will be your home page, lets put the basic stuff in it
```
<html>
<head>
    <title>My First HTML Page</title>
</head>
<body>
    My text goes here.
</body>
</html>
```
what happened? everything html has to be inside tags `<>` there are many different tags for different needs and we'll go over some of them here, the html tag is most basic one, note when you start a tag that has beginning and and end we'll add a `/` before the actual tag when we want to end it . so `<html>` starts it `</html>` will end it

the header tag is for everything at the top of our page, the body is everything in the middle of our page and there is also a footer tag that's not really needed for now ...

as soon as you made that `index.html` you can visit your newly created site which is your `github_name + .github.io`

here is mine [https://junguler.github.io/](https://junguler.github.io/)

### install VSCodium or another ide
i recommend you install vs codium which is a foss fork of vs code to make life easier, especially since it comes with many autocomplete features which cuts down and typing by quite a lot, install it from [here](https://vscodium.com/)

### some basic tags and how to use them
title: sets title of your page which is shown in the browser tab bar
```
<title>junguler</title>
```
p: sets up a paragraph to be written inside of it
```
<p>
my paragraph, can be many one or many lines
</p>
```
a: inserts link to a page
```
<a href="https://www.google.com/">google website</a>
```
img: add an image into your page
```
<img src="image.jpg" alt="some info">
```
br: makes a break between lines, like using inter in a text editor
```
<br> <p> stuff </> <br>
```
above code applies a break before and after our paragraph, sometimes you need to pass two breaks `<br><br>` to actually give two lines the one line distance we need. this could be two at the last part of above line, one on at the end of above line and on at the start of below line or two at the start of the below line.

### add files to your repo
you can add images, movies, music and many other things to your repo, i have made a `stuff` folder for this purpose. if you are working on the github web interface making a new folder is quite easy, click on `add file` on the top of your repo page click on `create a new file`. by default github puts your new file at the root directory of you repo but we want to make a new folder so in the name field at the top add a slash `/` to let github know we want to make a new folder, name your folder whatever you want and put another slash `/` after it and make an empty txt file like `1.txt` and click commit at the bottom.

the reason for making an empty file is github automatically removes empty directories/folders inside your repo, you can remove the empty txt file as long as you have at least one other file inside that folder which can be done by clicking `add file` and choosing `upload files`

### link a file that you uploaded in the directory in your page
lets assume i've uploaded a jpg file named `avatar` in my `stuff` folder, linking it to my page is easy
```
<img src="stuff/avatar.jpg"/>
```

### add favicon to your page
favicon are the little icons that show up at the left side of tab bar in your browser, altho we can use other image types for this lets do it by the book and convert it to a proper favicon using [this website](https://iconifier.net/) once you converted your image to favicon rename it to `favicon.ico` if it's not already and place it in the root directory of your repo, just hit `add file` then `upload files` method. now lets add it to our page
```
<link rel="shortcut icon" type="image/ico" href="favicon.ico"/>
```

### add styles to tags
styles are a very easy way to apply certain effects to the content of your tags, they sit right after you opened a new tag with `<tag style: > </tag>` lets apply a pink color to a paragraph to show and example:
```
<p style=color:pink >  everything is pink </p>
```
another example, lets apply a grey background color to the whole page using the body tag
```
<body style="background-color: #222;">
everything in the page is now with a background of grey
</body>
```
black text is hard to read in a grey background so lets make all the text in our paragraph have a white color
```
<p style="color: white;"> stuff
and things
are white
</p>
```

### add padding to our page
since monitor and displays are getting quite large in dpi we have to force everything in our site in the middle for the page to look better in all sizes of the screen, for this purpose we use the padding option. padding can be set many different things like pixels, centimeters and other things but the best option is percentage which takes to account the browsers windows size.
```
<div style="background-color:#333;color:#AAA;padding:3% 16% 3% 16%;">
```
i have this set at the top of my page because it has to be applied to everything in the page, this style has 3 arguments in it which are combined using `;`

first `background-color:#333` which sets the background color to the hex value of `#333` which a dark grey color

second `color:#AAA` sets the color of everything we haven't specifically set the color of the a bright grey

third `padding:3% 16% 3% 16%` pads the sides of our page to be shoved in the middle, it goes in the top, right, bottom, left order. so if i wanted to add more padding to the right i would of changed the second number

note: we are not making a mobile ready site as it's out of my level of knowledge and understating of html at this point, maybe we'll get to it some day

### add extra pages to our site
adding extra pages is easy, just make another `.html` file, if you don't plan on making many of these extra pages you could get away with putting all of them in the root directory and this makes linking to other pages of the same site easier but i'll opt to make an extra page names `pages` to keep everything organized 

our second page is named `second.html` which is inside our `pages` folder, everything we did on the main `index.html` can be applied to this page too but we remove duplicated information and put new things inside.

### link the second page to our homepage and vise versa
lets put a link at the top of both our pages to link them together 

in the `index.html` do:
```
<a href="pages/second.html" style="background-color:#444;color:white;font-size: 18px;">projects</a>  
```
here i called my second page `projects` but linked to `second.html` which is the actual name of the page

in the `second.html` do:
```
<a href="../index.html" style="background-color:#444;color:white;font-size: 18px">home</a>  
```
here we called our main page `home`, notice how we add `../` behind `index.html` because we want to go one page up/back to the root directory to link the main page

for our second page to find the favicon we also need to link it like this as well 
```
<link rel="shortcut icon" type="image/ico" href="../favicon.ico"/>
```
### add footer to our pages
footer stays at the end of our page and usually contains contact information or web hosting and technologies, lets start by opening a footer tag:
```
<footer>
</footer>
```
inside our first opened tag we will add some stylings:
```
<footer style="position: fixed;bottom: 2%;">
```
first part is `position` which we will set to fixed as we want it to always be shown, next is `bottom` which we will set to 2% which forces our footer %2 up, now lets add our info and include a link with yellow style coloring:
```
made with github's free web hosting, look <a style="color: yellow;" href="https://pages.github.com/">here</a> for more information
```
close your footer tag and we are good to go:
```
<footer style="position: fixed;bottom: 2%;">
made with github's free web hosting, look <a style="color: yellow;" href="https://pages.github.com/">here</a> for more information
</footer>
```
for my second/project page i opted to use the `relative` option for `position` which puts our footer at the end of the page's content since i didn't want it to be shown on the page, you can also use a fixed postion in such cases of long pages but you need to add some background color styling to differentiate it from the contents of the page.

### add white space in html
anything more than one space between two words in html is not recognized/shown in the page, we can get around this by adding `&nbsp;` for one space or use it multiple times `&nbsp;&nbsp;`, use `&ensp;` for two spaces and `&emsp;` for 4 space. just put them anywhere you want additional spaces

### align text to left and image to the right
this seems like a very small issue but unless you watch the website at 100% page zoom the image does not stay at the same place in relation to the text on the screen. we go around this issue by:

first adding style to our body tag `display: flex;` 
```
<body style="background-color: #222;display: flex;">
```
now float your image to the right side of the screen `float: right;`
```
 <img style="float: right;" src="stuff/avatar.jpg"; />
```
the last step is to make our paragraph have automatic width `width: auto;`
```
<p style="width: auto;">
paragraph goes here
</p>
```
### keep banner from overflowing the page
by default our banner image would overflow and get out of our page when zoomed in, add a overflow style to the whole page to keep this from happening:
```
<div style="background-color:#222;color:#ccc;padding:0% 16% 3% 16%;overflow: hidden;">
```
now force our banner to always keep at 100% width and keep our whole page padding too:
```
<img style="width: 100%;" src="stuff/h-banner.jpg" ><br>
```

### add go to top button
add a simple un-intrusive go to top button, upload your image or simply use text
```
<a style="position: fixed;bottom: 2%;right: 16%;" href="#"><img src="../stuff/up.png"></a>
```
every browsers sees `#` as the top of the page so we can use it as a link, lets fix it's position to to the bottom of the screen and 16% to the right, exactly like our page padding.

this is the most basic implementation i could find online, other methods involve assigning id inside tags and link them using the `#id`, here is an example of making a go to bottom button:

add foot id inside our footer
```
<footer id="foot"></footer>
```
link it
```
<a href="#foot">Go to bottom</a>
```

### change background color or use an image
in this example lets apply a gradient to our page using `background-image` style
```
background-image: linear-gradient(#333,#111);
```
we used a linear gradient and applied color `#333` to top of our page and `#111` to the bottom, because our margin color is also is set to `#111` the content of the page blends with the unused margins.

applying and image to our background is also easy:
```
background-image: url("background.jpg");
```
be mindful of the the image location, if it's in a folder you to have to link it accordingly, for way more examples on this check this [page](https://www.edureka.co/blog/background-image-in-html/) as it was how i learned it

### add some basic css
cascading style sheets or css are an easier way to have an orginized place for all of our styles and will help you write more efficiently and type less duplicate codes, so far we added all the styles we needed inside our tags using `style=""` but if we know we have some styles that are needed to apply to many things we can write the style once in our css file and have it used automatically for basic tags or manually add them as a class, so lets show some example of this

first of all, lets make a text file named `style.css` and link it at the top of our page, make sure to link this relativly to where your html page is located, in my case my second page is in a folder in our website directory so i use `href="../style.css"` for that page because we need to go up/back one page
```
<link href="style.css" rel="stylesheet" type="text/css">
```
for basic tags like `<p>` `<body>` that we want to always include and have a unified look for all of our pages we do this in our `style.css`:
```
body {
    background-color: #111;
}
```
the above style automatically gets used every time we use a `<body></body>` tag

for more specific style sheets we add a `.` before the style and manually apply it to our tags using `class=""`
```
.banner {
    width: 100%;
}
```
i just want to apply this style in my banner pictures so we do this:
```
<img class="banner" src="stuff/h-banner.jpg">
```
if you don't want the same style to be applied to basic tags like `<p></p>` in the above example remove that section from our style.css and make a custom class style for and apply it manually.
```
.mypara {
    text-align: center;
}
```
and add this custom class to a paragraph
```
<p class="mypara"> every text in this paragraph is centered </p>
```
and a paragraph that doesn't include this class will have a default and basic look

### write in markdown and convert to html
markdown is a very easy to write and style language that doesn't get in your way and it's extremely easy to write on, you can find some basic information on markdown formating on github [here ](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) 

there are tons of examples markdown files here on github or elsewhere to get your feet wet writing it and [here](https://bookdown.org/yihui/rmarkdown/) is another good tutorial website for it

now that we wrote our first markdown page we use an amazing project called [markdown-it](https://markdown-it.github.io/) to convert it to html, keep in mind that this is only one way of converting markdown to html and there are many other ways to do it either in your ide or external websites

copy your markdown text to the left side of the website and click source on the wirte side to copy the html text, copy it into an empty html page and lets add our usual start and end of every page to it and apply some css here and there where it doesn't look good and you already have a page styled and ready to go

```
<!doctype html>
<html lang="en">
   <link href="style.css" rel="stylesheet" type="text/css">
   <div class="pagebody">
<head>
    <meta charset="utf-8">
    <title>Junguler</title>
    <link rel="shortcut icon" type="image/ico" href="favicon.ico"/>
</head>
```
add the code you copied after these lines and end the page with your footer if you have one or just leave it empty

i'm planning to use this method to easily convert my markdown tutorials to pages for my website that look like they belong and written from scratch

update: converting 9 markdown tutorial pages to html only took 2 hours to get up and running, this is the fastest way of writing html i know of

### embed video in your page
for embedding video to our page we can use the `<video></video>` tag, we can also specify to always show the video controls and loop the video by placing them inside our opening tags `<video controls loop>` and then embed the video using `<source src="video.mp4" type="video/mp4"` we also specified the type of video we are embedding which is `video/mp4`
```
<video controls loop>
  <source src="video.mp4" type="video/mp4">
</video>
```
for making the video look right we also add width and height styling to the video tag, either manually:
```
<video style="width: 100%;height: auto;" controls loop>
```
or in our css stylesheet:
```
video {
    width: 100%;
    height: auto;
}
```

### make a nested menu at the top of the page
for making a nested menu we need to use two tags, first one is the ul tag `<ul>` which makes our menu entry and li tag `<li>` which lets us nest links inside it

the first step is to open a nav tag an put our ul and li tags inside
```
<nav>
    <ul class="nav">
      <li class="menu">
        <a href="first.html"> first menu entry </a>
      <li class="menu">
        <a href="second.html"> second menu entry </a>
        <ul>
          <li><a href="nested.html"> nested menu entry inside second menu </a></li>
        </ul>
      </li>
    </ul>
  </nav>
```
now for applying css, for our ul and li tags
```
ul {
    list-style: none;
}

li {
    position: relative;
}

li ul {
    display: none;
    position: absolute;
    background-color: #444;
    padding: 2px 6px 6px 6px;
}
  
li:hover ul {
    display: block;
}
```
notice that we have set differnt css styles for ul tags that have li tags inside them and also for overing over our menu entries, we also made some classes that we applied to our tags manually, .nav is being applied to the whole menu and is the most influencial in the overal look of your menu
```
.nav {
    position: fixed;
    background-color: #444;
    font-size: 20px;
    float: left;
    padding: 0px;
    display: flex;
    list-style: none;
    flex-direction: row;
}

.menu {
    display: inline-block;
    font-weight: bold;
}
```
like all the other examples so far if you are linking to a page that's not in the root of your blog directory you to change the links of your menu entries in you pages

unfortuently i lost the link to the page i've taken this information from but here is a usueful [page](https://www.w3.org/wiki/Creating_multiple_pages_with_navigation_menus) with more information

#### more stuff will be added as i learn ...
