# Intro to coding

This is a 2-hour course to help you get started in web development. As you can imagine, it's not possible to cover everything in just two hours so I've distilled it to just the essentials. I've also left some learning resources that you can follow up on after the course. 

The aim of this course is to give you a cursory introduction to

- how the web works,
- the components of a web page (HTML, CSS, and JavaScript), and
- to build your very own web page on [Codepen](https://codepen.io)

## The internet and the world wide web

![internet](https://waiukuelearning.wikispaces.com/file/view/books-internet.gif/126751571/books-internet.gif)

Learn more about the [web](http://marksheet.io/introduction.html).

## HTML basics

HTML stands for **H**yper**T**ext **M**arkup **L**anguage. Sounds fancy and it might even look intimidating, but we're going to see that HTML is nothing more than just plain text. Don't believe me? Let's prove it. 

### It's just plain text

![ice cream](https://s-media-cache-ak0.pinimg.com/originals/b8/7f/46/b87f462cdbe064a17e17022605cf0a98.jpg)

> HTML is like plain vanilla ice cream

For this exercise you'll need to use TextEdit\* (Mac) or Notepad (Windows) to create a file, add the text you see below, and save it as `webpage.txt` on your Desktop.

```txt
This is my first web page

Welcome to my first web page.
```

Now, open the file with your web browser.

> Think about how we could format this so that the first paragraph is a heading.

\* For Mac users, TextEdit will not allow you to save a file in `.txt` format by default. To do so, you'll have to change your default settings. Go to TextEdit preferences and select **plain text** under **Format**.

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

- [Dash](https://dash.generalassemb.ly/)

If you prefer to take an in-person course, there's [Frontend Web Development](https://generalassemb.ly/education/front-end-web-development) and [Web Development Immersive](https://generalassemb.ly/education/web-development-immersive) offered at [General Assembly](https://generalassemb.ly/) that go into much greater depth.

## About the instructor

Jesstern Rays is a software developer at [ThoughtWorks](https://thoughtworks.com) and an instructor at General Assembly. He is also a co-organizer of [SingaporeJS](https://www.meetup.com/Singapore-JS/) and the host of talk.js, a monthly JavaScript meetup.

Feel free to reach out to him on [Telegram](https://t.me/jsstrn), [Twitter](https://twitter.com/jsstrn), or [email](mailto:jessternrays+intro-to-coding@gmail.com?subject=[Intro%20to%20coding]&body=Hi%20Jesstern,).
