## Creating the website

**This is written in markdown, though it can easily be transferred into a docx format if you request I do so.**

*Markdown is a sort of html replacement, and also a successor to TeX (LaTeX)*

So let's begin!

## Part 1 - The Basics

#### Step 1 - getting the right stuff

To being, you're going to need to get the **theme** we're using. Run this command in your preferred terminal.
`git clone https://github.com/BlackrockDigital/startbootstrap-agency stekki/`

This command will copy all the files you need and put them into a folder called **stekki**, which is the name of our project.

Then, all you need to do is run this command and you should have everything more or less ready.

`npm install`

<img src="./essayPics/S1P1.png" width="500px" style="border-radius: 7px;">

<img src="./essayPics/S1P2.png" width="500px" style="border-radius: 7px;">

---

#### Step 2 - The Basics

You should have more or less everything you need set up now, so let's get on with the "development".

First of all, run the command `gulp`. This will compile the sass into css, and will start our website. It should automatically open it in your browser but just in case it doesn't, you should find it on `localhost:3000`.

I encourage anyone reading to try changing some text in the `html files`, as gulp has instant reloading, so any change you make will visible right away.

So to start, open up the `index.html` file in the main directory, just try changing the title to `stekki`. 

The text you should change is located on the *33rd and 11th* lines. 

*Note: I'm using vim as my text editor, though you can use whatever you want*

<img src="./essayPics/S2P1.png" width="600px" style="border-radius: 7px;">


---

#### Step 3 - The Basics Applied

Now that you know how to change text in html, it's time to do something with that knowledge.

This section is going to change some fundamental things on the website, such as the titles, though the other steps will be divided by the sections on the webpage and named accordingly 

I will just generally change the text on the website, and replace it with my text, just to get a feel for what it's like to edit this content. So let's start with the big heading on the *64th line*.

Since the layout here is a bit inverted, we'll just change that to say `Stekki`, and we'll change the line directly below it to say `The value of Bosnia`, just like in our design specification.

<img src="./essayPics/S2P2.png" width="800px" style="border-radius: 7px;">

---

#### Step 4 - Changing colors 

As we said in the specifications and most of all discovered through our research, colors are very important to the look and feel of a website, so let's change them up a bit.

In your website directory, you should have a folder called `scss`, and inside that another folder called `base`.
<br> Now I want you to go into that folder and edit a file called `_variables.scss`.

*Note: This is what's called a `sass` file, with it's file extension `scss` being short for `sassy css`. It basically allows us to do some pretty cool things, like we're about to.*

<img src="./essayPics/S4P1.png" width="550px" style="border-radius: 7px;">

*`_variables.scss` file before and after*

From here, all you need to do is, as shown in the image above, change the `$primary` value to `#D3EEBB`.

You should get something like this!

<img src="./essayPics/S4P2.png" width="650px" style="border-radius: 7px;">

*Sleek, professional design.*

I chose this specific color due to it being a nice, calming green tone, which represents our country and website quite well.

There's one more place where we need to change the color: 
<br> In `scss/components/_buttons.scss` change the color on the last line from `rgba(254, 209, 55, .5)` to `#abdf7e`

This should give us the exact color scheme we want to have here.

---

#### Step 5 - Menu Items

To finish off this section of the essay, lets go ahead and change the menu buttons to say what we want them to say.

Now there are many parts to this page, and we're going to make use of every single one.

So, around `line 32`, you'll see a list of the items looking something like this:

<img src="./essayPics/S5P1.png" width="500px" style="border-radius: 7px;">

Now you can just change the **white values** to whatever you want and the change should reflect on the site.

Going off of the design specifications, we'll do the following.

`Bosnia | Stekki | History | Coolness | Contact`

And after making the change you should get something along the lines of:

<img src="./essayPics/S5P2.png" width="500px" style="border-radius: 7px;">

##### *Deviation 1

This is the first time during this project that we deviate a little from our original design.
<br> Even though I thought it was okay, after making it I saw how bad it looked on mobile devices, so we're gonna go with the one that's already here.

## Part 2 - Organization

#### This section focuses on large website changes

We'll mostly just be moving the actual files around and getting everything organized and set up, removing junk that we don't need and such, so you could consider this a little boring- I certainly do, but it is essential.

---

#### Step 1 - The physical files 

For this part, I'll be using windows explorer and vim, again, literally anything works.

Now open your working directory, the place with all the files. If you're in a terminal on windows (even using WSL), just doing `explorer.exe .` will work.

The first- and most essential step, is deleting anything ending in `.php`, I will not allow php on the website.
<br> In all seriousness, aside from being a bad language, we will not support php since the free hosting provider we'll be using won't support it. I may just do mailing in javascript later on, but we'll see.

So, I want you to delete the `mail` folder, since we won't be needing it.

// TREMOVE: removed most of the section cause it seemed pointless

#### Step 2 - Erasure

Heading over to your `index.html` file, it's time to get rid of some of it, since it's code we don't need at the moment.

