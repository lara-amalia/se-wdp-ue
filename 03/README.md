# WDP3 – Exercise 3

CSS Basics: Let's add some styling to our website we started to create in the first exercise. This time we will add text styles, colors and spacings.

## The styles.css file

For this website we will create one single CSS file that contains all our styles. (You can also split your code up into more than one file, but don't forget to link all of them in the HTML files where you need them.)

Create a file called `styles.css` next to your `index.html` file and add a link to it in the head of your HTML file.

```html
<link rel="stylesheet" href="styles.css" />
```

For a quick check if everything works, set the background-color of your whole page to red and have a look at your index page in the browser.

```css
body {
  background-color: red;
}
```

> Note: Don't forget the semicolon after each CSS rule!

Also reference the stylesheet in all other HTML files (about, portfolio, contact).

### Text

Choose two fonts for your website from [Google Fonts](https://fonts.google.com). Use one for headlines and the other one for body text. You can also use one font and select the regular style for the body text and the bold style for headlines.

> If you found a font you like, check out the font pairings suggested by Google Fonts, maybe there's another one you can use as second font.

Copy and paste the `link` you can find in the embed-tab into the head of your HTML files.

Define the `font-family` for your website in the CSS file. Don't forget to add a fallback font.

```css
body {
  font-family: "Source Sans Pro", Helvetica, Arial, sans-serif;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: "Other Font", Helvetica, Arial, sans-serif;
}
```

Play around with `text-alignment` – maybe center your headlines?

You could also set `text-transform` to `uppercase` for headlines, or for the links in your navigation?

### Colors

Change the font color for your website. Use a different color for headlines and body text.

### Links

Define styles for your links. Choose a color, define whether they should be underlined or not, add a hover style…

```css
a {
  color: #1acc78;
  text-decoration: none;
}

a:hover {
  background-color: #efefef;
}
```

### Lists

Change the look of lists on your website.

## Website design – Let's make a plan

Before adding more styles, we need to make a plan how the website should look like in the end. I prefer using pen and paper for that.

Defining a page structure is also part of web development. Based on a design (done by yourself or by a web designer) we have to decide how to enhance the HTML code in order to implement the given design.

For our first website let's keep it clean and simple.

<!-- ToDo: insert sketch -->

## The CSS box model

<!-- ToDo: paddings / margins -->

## Portfolio overview tiles

<!-- ToDo: similar to movies overview page -->
