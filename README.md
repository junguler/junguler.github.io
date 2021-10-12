my work in progress website, the old markdown file was moved to [old-README.md](https://github.com/junguler/junguler.github.io/blob/main/old-README.md) for archivable purposes and i try to explain what i've learned better this time

### quick links
 * [first step](https://github.com/junguler/junguler.github.io#first-step)
 * [make index.html](https://github.com/junguler/junguler.github.io#make-indexhtml)
 * [vscodium](https://github.com/junguler/junguler.github.io#install-vscodium-or-another-ide)
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
this seems like a very small issue but unless you watch the website at 100% page zoom the image does not stay at the same place in relation to the text on the screen. we go around this issue buy:

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

#### more stuff will be added as i learn ...
