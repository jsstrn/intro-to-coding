# Intro to coding

This is a 2-hour course to help you get started in web development. As you can imagine, it's not possible to cover everything in just two hours so I've distilled it to just the essentials. I've also left some learning resources that you can follow up on after the course. 

The aim of this course is to give you a cursory introduction to

- how the web works,
- the components of a web page (HTML, CSS, and JavaScript), and
- to build your very own web page on [Codepen](https://codepen.io)

What you'll need for this course

- a laptop with a decent Internet connection
- a web browser (Chrome or Firefox)
- TextEdit (Mac), Notepad (Windows), or some equivalent application
- Pages (Mac), Word (Windows), LibreOffice (Linux), or some equivalent application
- a Codepen account (you'll have to create one [here](https://codepen.io)
- participate in the course (answer questions, ask questions, don't just watch; try out the activities)
- a lot of the activities and questions in this course requires you to think, so don't look ahead at the answers

We'll be building a simple web page in Codepen as we work through the content of this course. Here's an [example](https://codepen.io/jsstrn/full/pPEeMr/).

## The Internet and the Web

![internet](https://waiukuelearning.wikispaces.com/file/view/books-internet.gif/126751571/books-internet.gif)

The Internet is a interconnected network of computers which communicate through protocols. A subset of the Internet is the Web which uses the `HTTP` and `HTTPS` protocols to communicate.

### Clients and servers

Very briefly, a connection between computers on the web can be divided into two camps

- Clients want information. They make requests to servers for information
- Servers have information. They respond to client requests with information

Clients include your web browser (Firefox), email client (Outlook), a messaging app (Telegram).

Learn more about the [web](http://marksheet.io/introduction.html).

## HTML basics

HTML stands for **H**yper**T**ext **M**arkup **L**anguage. Sounds fancy and it might even look intimidating, but we're going to see that HTML is nothing more than just plain text. Don't believe me? Let's prove it. 

### It's just plain text

![ice cream](https://s-media-cache-ak0.pinimg.com/originals/b8/7f/46/b87f462cdbe064a17e17022605cf0a98.jpg)

> HTML is like plain vanilla ice cream

For this exercise you'll need to use TextEdit\* (Mac) or Notepad (Windows) to create a file, add the text you see below, and save it as `webpage.txt` on your Desktop.

\* For Mac users, TextEdit will not allow you to save a file in `.txt` format by default. To do so, you'll have to change your default settings. Go to TextEdit preferences and select **plain text** under **Format**.

```txt
This is my first web page

Welcome to my first web page.
```

Now, open the file with your web browser.

> Why don't we just use `.txt` files to create web pages?

The reason why we don't use `.txt` files is that we are not able to format them. We need a way to format our `.txt` file so that its much easier to read. That's where HTML comes in - HTML is just plain text with a bit of markup.

### Creating your first web page

Let's now rename our `webpage.txt` file to `webpage.html`. Now let's open it again in our web browser.

Wait! All our paragraphs are combined! Looks like the web browser is unable to tell where one paragraph ends and where another begins. We need to help it out by giving it a special marking (or markup).

### Creating your own syntax

> Let's imagine you're tasked to create this sort of marking for each paragraph. What would yours look like? Remember, your markup has to indicate to the browser the start and end of a paragraph.

Here's what some students have come up with

- [paragraph-start]This is my first paragraph[paragraph-end]
- [p-start]This is my first paragraph[p-end]
- #p$This is my first paragraph$p#

### HTML syntax

Indeed, a paragraph in HTML is very similar to any of these suggestions. Here's what a paragraph element in HTML looks like

```html
<p>This is my first paragraph</p>
```

> Think about how we could format this so that the first paragraph is a heading instead.

The paragraph element is made up of an opening tag `<p>` and a closing tag `</p>`.

We can place attributes in the opening tag. Think of attributes as distinct properties of an HTML element. For instance, we might have two buttons with distinct styles (CSS) and behaviors (JavaScript).

```
<button class="buy-now-btn">Buy Now</button>
<button class="cancel-btn">Cancel</button>
```

### Looking under the hood

![car mechanic cartoon](https://i.imgur.com/XVSzNmL.jpg)

Let's look under the hood to see how this web page was built. Right click on this web page and select **Inspect** (some browsers might show **Inspect Element**).

Locate the text "Intro to coding," it should look something like this

```html
<h1>Intro to coding</h1>
```

### Structure of an HTML document

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Page title</title>
  </head>
  <body>
    <h1>This is a heading</h1>
    <p>This is a paragraph</p>
    <p>This is another paragraph</p>
  </body>
</html>
```

The HTML code above can be represented in the image seen below.

![](https://kumarsher45.files.wordpress.com/2015/01/html-5-page-structure.jpg)

The `root` element is `<html>` and it only has two children, `<head>` and `<body>`. Only elements in `<body>` are displayed in the browser. Also notice that child elements are indented to make it easier to read (we say these elements are nested).

### Inserting images

Image tags are a little different. Since there is no text content that an image tag needs to wrap around there's no need for a closing tag i.e. `</img>`. The `src` attribute stands for source and the `alt` attribute refers to the alternative text describing the image.

The source is the path or URL to the location of your image. Try looking under the hood of an image to see where its source is from.

```
<img src="kittens.jpg" alt="Here be kittens">
```

We'll be using images from [Pexel](https://www.pexels.com/) when building our web page later.

Learn more about [HTML](http://marksheet.io/html-basics.html)

### Links

Here's how we would create a link to an internal web page within your website.

```
<p>Go to <a href="another-page.html">my other page</a>.</p>
```

Here's how we would create a link to an external website.

```
<p>Go to <a href="https://duckduckgo.com">DuckDuckGo</a>.</p>
```

## CSS basics

A CSS rule comprises of a selector and its declaration block (that's what's inside the curly braces). A declaration block contains the properties and the values you want to set.

```css
selector {
  property: value
}
```

CSS is also not a programming language; it's just a set of rules that the browser uses to style its content.

## Heading out with style

Before we learn to style a heading on a web page with CSS, let's first look at how we would do it in Pages (Mac) or Word (Windows). We would type our heading, then select it, increase its font size and maybe even its font weight to bold.

How does this look like in CSS? We could apply these rules to the paragraph element, but this would apply to all paragraph elements.

```css
p {
  font-size: 2rem;
  font-weight: bold;
}
```

A better way might be to uniquely identify that specific paragraph with the `id` attribute in your HTML element. That way we can access it using the `id` selector in CSS.

In your HTML file, write:

```html
<p id="heading">Intro to coding</p>
```

In your CSS file, write:

```css
#heading {
  font-size: 2rem;
  font-weight: bold;
}
```

You can also use the `class` attribute.

In your HTML file, write:

```html
<p class="heading">Intro to coding</p>
```

In your CSS file, write:

```css
.heading {
  font-size: 2rem;
  font-weight: bold;
}
```

The difference is that `class` attributes are meant for styling a logical group of elements (e.g. a navigation bar or list items) while `id` attributes are meant for styling only that particular element. As such, it's more common to use `class` than `id` attributes.

In fact, there is a heading tag in HTML that we can use `<h1>`, `<h2>`, ..., `<h6>`. That would be better than using the `<p>` for headings.

![ghost fashion](http://www.digitalcitizen.life/sites/default/files/img/book_buildwebsite/buildwebsite_6.png)

Learn more about [CSS](http://marksheet.io/css-basics.html)

## JavaScript basics

It is beyond the scope of this course to cover JavaScript, but do realize that JavaScript is an important part in web development. The only programming language that browsers can understand is JavaScript, so if you want to build interactive websites you'll typically need to use JavaScript to do so. 

Just like there are numerous languages in the world, there are also numerous programming languages out there. You might have heard of programming languages such as Python, Ruby, Java\*, or even C++, but only JavaScript can be interpreted by the browser.

\* **JavaScript is not Java**. They are both programming languages, but they are entirely different and completely unrelated. Remeber, Java is to JavaScript as car is to carpenter. 

### Math 101

Type `1 + 1` in your browser console and hit `Enter`.

```
> 1 + 1
```

A programming language is able to evaluate a mathematical expression and just like in mathematics you can also store these values in variables.

```
> x = 1 + 1
```

Now, if you ask the console to evaluate `x` it will return `2`.

If you're keen to learn JavaScript, head over to the next section where I provide some online learning resources to go beyond this course.

## Learning beyond this course

- [Dash](https://dash.generalassemb.ly/) - I would highly recommend this short course. You'll learn to create a portfolio web page in HTML and style in with CSS
- [Frontend Web Development](https://generalassemb.ly/education/front-end-web-development) - a part-time in-person 10-week course, there's [FEWD](https://generalassemb.ly/education/front-end-web-development) and
- [Web Development Immersive](https://generalassemb.ly/education/web-development-immersive) - a full-time in-person 12-week course offered at [General Assembly](https://generalassemb.ly/)

## About the instructor

Jesstern Rays is a software developer at [ThoughtWorks](https://thoughtworks.com) and an instructor at General Assembly. He is also a co-organizer of [SingaporeJS](https://www.meetup.com/Singapore-JS/) and the host of talk.js, a monthly JavaScript meetup.

Feel free to reach out to him on [Telegram](https://t.me/jsstrn), [Twitter](https://twitter.com/jsstrn), or [email](mailto:jessternrays+intro-to-coding@gmail.com?subject=[Intro%20to%20coding]&body=Hi%20Jesstern,).
