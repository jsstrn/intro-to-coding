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

## The internet and the world wide web

![internet](https://waiukuelearning.wikispaces.com/file/view/books-internet.gif/126751571/books-internet.gif)

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

### Looking under the hood

![car mechanic cartoon](https://i.imgur.com/XVSzNmL.jpg)

Let's look under the hood to see how this web page was built. Right click on this web page and select **Inspect** (some browsers might show **Inspect Element**).

Locate the text "Intro to coding," it should look something like this

```html
<h1>Intro to coding</h1>
```

Learn more about [HTML](http://marksheet.io/html-basics.html)

## CSS basics

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

![ghost fashion](http://www.digitalcitizen.life/sites/default/files/img/book_buildwebsite/buildwebsite_6.png)

CSS is also not a programming language; it's just a set of rules that the browser uses to style its content.

Learn more about [CSS](http://marksheet.io/css-basics.html)

## JavaScript basics

JavaScript is a programming language and it's the only one your web browser understands. Just like there are numerous languages in the world, there are also numerous programming languages out there. You might have heard of programming languages such as Python, Ruby, Java\*, or even C++, but only JavaScript can be interpreted by the browser. 

\* JavaScript is not Java. They are both programming languages, but they are entirely different and completely unrelated. Remeber, Java is to JavaScript as car is to carpenter. 

## Learn beyond this workshop

- [Dash](https://dash.generalassemb.ly/) - I would highly recommend this short course. You'll learn to create a portfolio web page in HTML and style in with CSS
- [Frontend Web Development](https://generalassemb.ly/education/front-end-web-development) - a part-time in-person 10-week course, there's [FEWD](https://generalassemb.ly/education/front-end-web-development) and
- [Web Development Immersive](https://generalassemb.ly/education/web-development-immersive) - a full-time in-person 12-week course offered at [General Assembly](https://generalassemb.ly/)

## About the instructor

Jesstern Rays is a software developer at [ThoughtWorks](https://thoughtworks.com) and an instructor at General Assembly. He is also a co-organizer of [SingaporeJS](https://www.meetup.com/Singapore-JS/) and the host of talk.js, a monthly JavaScript meetup.

Feel free to reach out to him on [Telegram](https://t.me/jsstrn), [Twitter](https://twitter.com/jsstrn), or [email](mailto:jessternrays+intro-to-coding@gmail.com?subject=[Intro%20to%20coding]&body=Hi%20Jesstern,).
