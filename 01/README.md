# WDP3 – Exercise 1

HTML Basics: Let's create your first small website! This will be a portfolio page with a startpage (index), an about me page, a subpage that lists all your development projects and a contact page.

## 1 The index.html file

Create the root folder for your first WDP3 website, e.g. `wdp3-website`, and add an `index.html` file. Open this file in a text editor (like "Visual Studio Code" or another editor of your choice).

### 1.1 Basic HTML file structure

Every HTML file consists of a doctype, the wrapping `html` element, that contains the page's `head` and `body`.

Add a `title` to your page head section and verify it's displayed in the browser's tab bar.

Define the document's language and character encoding.

Duplicate the index file (name it e.g. `index-base.html`) before adding content, because we will need the basic file structure for other subpages as well.

### 1.2 Index page content

Your index page should contain the following content:

- a page tilte (`h1`)
- a short introduction (`p`)
- a subsection containing a list of projects you already worked on (`h2` headline, `ul` unordered list)
- another subsection containing a `table` displaying technologies and programming languages you already worked with, where and when you first heard about it, in how many projects you already used it, and maybe other interesting facts that come to your mind. The table could look like this:

| Technology | Learning since | Skill level | Number of projects |
| ---------- | -------------- | ----------- | ------------------ |
| HTML       | 2003           | Advanced    | 23                 |
| CSS        | 2003           | Advanced    | 20                 |
| JavaScript | 2005           | Advanced    | 8                  |
| TypeScript | 2016           | Medium      | 5                  |
| Java       | 2010           | Beginner    | 3                  |
| ...        | ...            | ...         | ...                |

Use a table caption (`caption`), table rows (`tr`), table header cells (`th`) for the columns' headlines, and table cells (`td`) for the content.

You can find some table examples in the [MDN table documentation][1]

## 1.3 Other subpages

Create some more HTML pages using the content of the `index-base.html` file we duplicated at the beginning. We will need the following files, which should be located next to the existing `index.html` file:

- contact.html
- portfolio.html
- about.html

## 2 Page structure and navigation

Back in our `index.html` file, let's take some time to add structure using the following tags:

- `nav` for the navigation
- `header` for the header
- `main` for the main content
- `section` for content sections
- `footer` for the page's footer

The page then could look similar to the following code snippet:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Lara's personal website</title>
  </head>
  <body>
    <nav>
      <!-- the page's navigation, exercise 2.1 -->
    </nav>
    <header>
      <h1>Lara's personal website</h1>
      <p>
        This website was created during the WDP3 exercises and contains
        interesting information about some of my programming projects.
      </p>
    </header>
    <main>
      <section>
        <h2>Welcome to my website!</h2>
        <p>
          <!-- some text about you and the purpose of this website (exercise 1.2) -->
        </p>
      </section>
      <section>
        <h2>My projects</h2>
        <ul>
          <!-- a list of projects you worked on or are currently working on (exercise 1.2) -->
        </ul>
      </section>
      <section>
        <h2>Technologies</h2>
        <table>
          <!-- the table from
         exercise 1.2 -->
        </table>
      </section>
    </main>
    <footer>
      <p>
        This website is built with love in Hagenberg, Upper Austria.<br />
        &copy; 2020
      </p>
    </footer>
  </body>
</html>
```

### 2.1 Navigation

For our small website, we need a navigation to connect the homepage and the other subpages. A navigation consists of links, in our case we have the following ones:

- a link to the homepage
- a link to the about page
- a link to the portfolio page
- a link to the contact page

```html
<nav>
  <a href="./index.html">Home</a>
  <a href="./about.html">About me</a>
  <a href="./portfolio.html">Portfolio</a>
  <a href="./contact.html">Contact</a>
</nav>
```

It's not neccessary to include a link to the currently active page (in our case: the index page). But to be able to reuse this navigation snippet easily on the upcoming subpages, we add all four links to the navigation.

## 3 About me page

The about page only contains the basic HTML structure from exercise 1.1. Add some content about you. Start with a `h1` headline (can be nested in a `header` element), add some text about you (use `p` elements), add a short CV using a list and list items (`ul`, `li`). The content of your page should be wrapped by a `main` tag.

Use the same navigation and the footer from the index page (copy & paste).

### 3.1. Add an image

On the about page, add an image of you, using the `<img>` tag. Don't forget to add an alternative text (`alt` attribute).

The image file can be placed in an additional `images` folder next to your HTML files. The code you have to include in your file could look like this snippet:

```html
<img src="./images/lara.jpg" alt="Lara Aigmüller" />
```

> Remember: the image tag is self-closing and has no content.

## 4 Contact page

On the contact page we include a small contact form and additional address data.

The contact page also has an `h1` page title, a `main` section (which contains the main content), a navigation and an optional `footer`, which can be copy-pasted from the index page again.

### 4.1. Contact form

The contact form should at least include the following fields:

- name input (required)
- email input (required)
- age input (minimum age is 14)
- selection (country or favorite pet or favorite time of the year or …)
- message textarea
- newsletter checkbox
- submit button

If you have some time left, you can also play around with other input types, e.g. `color`, `date`, `radio`,…

> Don't forget to add labels to all your input fields.

### 4.2. Contact data

Below (or above) the form you can add some contact data. You can simply use a `p` element or make use of the `address` element, which is also available in HTML. You can find usage details in the [MDN address documentation][2].

## 5 Developer tools

There's a very useful tool you'll probably need every time you're developing something (a website or a web application) in your browser: the browser's developer tools. There are several ways to open them:

- right-click on an element (e.g. the headline of your page) and select Inspect or Inspect Element (depends on the browser)
- in Chrome: navigate to "View" - "Developer" - "Developer Tools"
- in Firefox: navigate to "Tools" - "Web Developer" - "Toggle Tools"
- or remember the Shortcut Option+Command+I (Mac) or Control+Shift+I (Windows, Linux)

Once opened, select the Elements-tab (Chrome), or the Inspector-tab (Firefox). Then you should be able to see the code you just wrote in your text editor right next to the rendered output.

With the developer tools open you can modify the website directly in the browser, play around with CSS (we'll do that next time), search for bugs and much more…

From now on, always keep the developer tools open while working on your website.

[1]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table#Examples
[2]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/address
