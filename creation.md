## Creating the website

**This is written in markdown, though it can easily be transferred into a docx format if you request I do so.**

*Markdown is a sort of html replacement, and also a successor to TeX (LaTeX)*

So let's begin!

You can follow along with the code <a href="https://github.com/theqoobee/stekki" target="_blank">here</a>.

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

*Note: I'm using vim as my code editor, though you can use whatever you want*

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

Inside the file, find this snippet of code:

```html
<section class="page-section" id="services">
  <div class="container">
```

Now delete everything between it and:

```html </div>
</section>
```

You should be left with this:

```html
<section class="page-section" id="services">
  <div class="container">

  </div>
</section>
```

Now do the same with the `teams (Coolness)` section. The end result should be:

```html
<section class="bg-light page-section" id="teams">
  <div class="container">

  </div>
</section>
```

And for the last step, delete the entire `teams` section.

Saving and refreshing the page should now reveal two empty sections (plus one missing) where the old ones used to be, which means we have everything we need to build the website, more or less exactly as our design suggests.

## Part 3 - The Layout

This section will cover setting up the layout of the website

So at this point we have everything more or less like we need it, a `blank section`, a section with `some pictures`, a section with a `tree structure` for the history, another blank section, and the `Contact Us` section.

We'll be using bootstrap's grid layout instead of the built in css-flexbox, simply because it's built into this template.

So let's start filling this in!

#### The services section

Go to the `Services` section, the first one we emptied, and add this inside it, just to see the concept.

The way bootstrap works is is divides your website into a grid of rows an columns. Every row is split up into 12 columns, due to the number being very good friends with division. You can have as many rows as you want, but only 12 columns per row.

Below we first define a row, then inside it add `two columns`, each the width of 6, meaning they will each take up half the screen since 6 is half of 12.

```html
<div class="container-fluid">
  <div class="row">
    <div style="background-color: lightgrey;" class="col-6">
      Hello world
    </div>
    <div style="background-color: lightblue;" class="col-6">
      Hello World Two
    </div>
  </div>
</div>
```

Refreshing the page, you should see this:

<img src="./essayPics/S7P1.png" width="500px" style="border-radius: 7px;">

Pretty basic, huh.

This is more a proof of concept than anything else, so it's time to put some content into this.

So let's add a proper placeholder for now:

*\*Note that the `col-md-6 col-sm-12` indicates that on medium displays (960px+), the sections are going to be next to each other, whereas they'll stack on smaller screens. This is a key point in **responsiveness***

```html
<!-- Services -->
<section class="page-section" id="services">
  <div class="container">
    <div class="row">
      <!-- The text column -->
      <div style="background-color: lightgrey; padding: 10px;" class="col-md-6 col-sm-12">
        <h2>Why are <strong>Stecci</strong> cool?</h2>
        <br>
        <p>This is a basic placeholder to make this look like there's text here so there's text</p> </div>
      <!-- The picture column -->
      <div style="background-color: lightblue; padding: 10px;" class="col-md-6 col-sm-12">
        <img src="img/nice.jpg" alt="An iamge" width="100%">
      </div>
    </div>
  </div>
</section>
```

Here's what you should get:

<img src="./essayPics/S7P2.png" width="500px" style="border-radius: 7px;">

I know- it looks like 2002, but hold your horses since this *is* just the layout section. <a href="https://www.saatchiart.com/art/Painting-colourful-landscape/1073491/4153627/view" target="_blank">This</a> is the image used, we're going to change that later, it's temporary, found it on my computer.

Also, notice that if you make the width of your browser window physically smaller, or depending on your pc settings even open the site on your phone, the columns are going to *responsively* stack.

#### The picture section

This is where we run into our next deviation from the design, just looking at this, it's obvious we can do more than what's presented in the design. The reason for this, similar to the first one is first of all design responsiveness, but even more importantly the general feel of the website, why not go a little more advanced.

We will use the already built in `bootstrap modals` to create this section. The idea is the following:

Three pictures displayed in a row, stacked on mobile of course, and upon pressing on one of the pictures a screen should pop up with a description of the place. This is good because

* It's a lot prettier
* It shows off `technical skill`
* Shows stekki in an even brighter light, bringing story to the pictures

Let's get on with it then!

To begin with, we need to **clear out** the stuff we don't need.

Scroll down to the `Portfolio` section, you should notice 6 `div` elements with the class of `portfolio-item`, pick and delete the last three, just so you're left with this.

```html

  <!-- Portfolio Grid -->
  <section class="bg-light page-section" id="portfolio">
    <div class="container">
      <div class="row">
        <div class="col-lg-12 text-center">
          <h2 class="section-heading text-uppercase">Portfolio</h2>
          <h3 class="section-subheading text-muted">Lorem ipsum dolor sit amet consectetur.</h3>
        </div>
      </div>
      <div class="row">
        <div class="col-md-4 col-sm-6 portfolio-item">
        ...
        </div>
        <div class="col-md-4 col-sm-6 portfolio-item">
        ...
        </div>
        <div class="col-md-4 col-sm-6 portfolio-item">
        ...
        </div>
  </section>
```

It's perhaps a little trickier, but now it's time to delete the corresponding modals. Using your editors `find function`, usually bound to CTRL+F (*Every editor has one, even notepad*), you should find the `Portfolio Modals` part of the html documents, it should have modals corresponding to the numbers of the portfolio cards.

Since we deleted the last three above, we do the same here.

<img src="./essayPics/S7P3.png" width="500px" style="border-radius: 7px;">

If you want to, clear out all the text in the modals, just for easier viewing, though it's optional.

That's all that really need be done here, let's move on to the next section.

#### The history section

Now there are great react and vue UI components for this exact thing, though using a frontend framework is outside of the cope of this "tutorial", so we gotta use what we have- what's already there.

I feel as though just editing the tree structure already present will be more than sufficient, since it will perfectly fit our criteria, so let's skip this for now, since there really isn't anything we need to do about the layout.

#### The 😎 coolness 😎 section

Since, as in the design, it's more or less the same as the first section, just copy that over, not much more to it for now.

```html
<!-- Cool -->
<section class="page-section" id="services">
  <div class="container">
    <div class="row">
      <!-- The text column -->
      <div style="background-color: lightgrey; padding: 10px;" class="col-md-6 col-sm-12">
        <h2>Why are <strong>Stecci</strong> cool?</h2>
        <br>
        <p>This is a basic placeholder to make this look like there's text here so there's text</p>
      </div>
      <!-- The picture column -->
      <div style="background-color: lightblue; padding: 10px;" class="col-md-6 col-sm-12">
        <img src="img/nice.jpg" alt="An iamge" width="100%">
      </div>
    </div>
  </div>
</section>
```


#### The contact section

There is absolutely nothing we need to change here, so just continue along.

#### *That marks the end of this section, there's not much left.*
---

## Part 4 - Content

Now, this is where we add actual content to the site, so let's get started right away.
