my work in progress website, i moved this markdown file to the old-README.md for archival purposes, i'll try to explain what i've learned better this time

### first step
make a github account, start a new repo with your user name and add `.github.io` at the end of it

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
you can add images, movies, music and many other things to your repo, i have made a `stuff` repo for this purpose. if you are working on the github web interface making a new folder is quite easy, click on `add file` on the top of your repo page click on `create a new file`. by default github puts your new file at the root directory of you repo but we want to make a new folder so in the name field at the top add a slash `/` to let github know we want to make a new folder, name you folder whatever you want and put another slash `/` after it and make an empty txt file like `1.txt` and click commit at the bottom.

the reason for making an empty file is github automatically removes empty directories inside your repo, you can remove the empty txt file as long as you have uploaded one other file inside that folder which can be accessed by clicking `add file` and choosing `upload files`

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
