# Intro to JavaScript

JavaScript is the de facto language of the internet. It's a tool that, once
mastered, will allow you to interact with users via apps in fun and
interesting ways.

In technobabble, JavaScript is a dynamic, untyped, and interpreted programming
language; it is prototype-based and supports both object-oriented and functional
approaches. What all this means will become more apparent in lessons and through
exposure to the language. But here are the basics.

## Objectives
+ Print JavaScript to the console
+ Explain proper use of semicolons and other syntax basics
+ Explain truthy and falsey values


## Syntax Basics

#### Variable Declaration

In JavaScript, to declare a local variable (which is almost always what you want
to do), you add the keyword `var` before the variable name, like so:

```javascript
var greeting = "hello world";
```

Well, this code is all fine and dandy but how do you run it? The best, possibly
most powerful thing about JavaScript is that all modern browsers know how to run
it. Then open up your browser's console. That's right, your browser runs a
JavaScript sandbox when you open up the console.

To open up your browser's console from Chrome, type `command` + `option` + `J`.
From Firefox, type `command` + `option` + `K`.

From your console, simply type the code above into the prompt and hit `return`.
There, you've run your first JavaScript code! (It assigned the string `"hello world"`
to the variable `greeting`.)

Open up Chrome and on any tab (even a blank one) right click and select
`Inspect` from the dropdown. From there, select the `console` tab:

![console](https://s3.amazonaws.com/learn-verified/console.png)

The white space below is your console, a sandbox where you can enter and execute
any JavaScript code you want.

![Executing JavaScript in Console](https://s3.amazonaws.com/learn-verified/exectuing-js-in-console.png)

With your console open, declare the `greeting` variable

```javascript
var greeting = "hello world";
```

then enter:

```javascript
console.log(greeting)
```

You should see "hello world" followed by `undefined`. `undefined` is the value
that the `console.log()` function returns.

`console.log()` is, as you probably noted, a function that prints its arguments
to the `console` (that little sandbox-y window that's now opened in your
browser). (As you might have guessed, "log" is a computer-y way of saying
"print".)

If that all seems a little complicated right now, don't worry — it'll make sense
soon, when we learn about objects, and functions, and arguments...

#### Whitespace

JavaScript gives whitespace no meaning outside of quotation marks.

```javascript
var greeting =         "hello world";

greeting === "hello world" // true
```

Whitespace enhances readability, but has no special meaning.

```javascript
var tvShows = {
  "ABC": [
    "The Bachelorette",
    "Grey's Anatomy"
  ],
  "FOX": [
    "Bones",
    "Empire"
  ]
};
```

Nowadays, most JavaScript developers use "soft tabs" at two spaces — in other
words, code is indented two spaces at each new level.

#### Semicolons

Semicolons *must* be used in some cases, *can* be used in others, and other
times aren't used at all.

**Necessary**

Semicolons must be used when two statements are on the same line (this is called
"statement chaining"). Here's an example:

```javascript
var fox = "XOF NWORB KCIUQ EHT";
fox = fox.split("").reverse().join(""); fox = fox.toLowerCase();
// => "the quick brown fox"
```
Of course, there are exceptions. For instance, when we cover loops, you may
notice that the `for` loop abides by this rule for the first two statements in
its argument but not for the last.

**Ideal**

From [Codecademy's blog on semicolons](https://www.codecademy.com/blog/78):

> As we saw above, the semicolon in JavaScript is used to separate statements.
> However, it can be omitted if the statement is followed by a line break (or
> there’s only one statement in a {block}). A statement is a piece of code that
> tells the computer to do something. Here are the most common types of
> statements:

```javascript
var i;                        // variable declaration
i = 5;                        // value assignment
i = i + 1;                    // value assignment
i++;                          // same as above
var x = 9;                    // declaration & assignment
console.log("hi");            // function call
```

> All of these statements can end with a `;` but none of them must. However, it
> is a good habit to terminate each statement with a `;`.

**Avoid**

Semicolons don't follow the closing curly brackets of `if`, `for`, `while`, and
`switch` blocks. For instance, this if statement has no ending semicolon:

```javascript
var lunchtime = true;

if (lunchtime) {
  console.log("Go get lunch!");
}
```

The above-mentioned cases are pretty easy to remember. It's a bit trickier to
remember that semicolons follow **function expressions** but not **function
declarations**.

``` javascript
// function declaration (no semicolon)
function foo() {
  return 'foo';
}

// function expression (semicolon)
var bar = function() {
  return 'bar';
};
```

Also avoid putting semicolons between an ending parenthesis and a beginning
curly bracket. In other words, you shouldn't write `) ; {`.

**Hints**

Should you get stuck with your semicolon usage (and don't worry, even
professional JavaScript developers occasionally forget what goes where), paste
your code into a JSLinter, such as [JSLint](http://www.jslint.com/) or even
[JSFiddle](http://jsfiddle.net/). If you click `Lint`, you'll see a line-by-line
evaluation of your semicolon usage and other syntax mistakes.

**A slightly more heretical take on semicolons**

Semicolons don't really matter in JavaScript. If we're working on a large
JavaScript application, chances are we're at least using a [minifier](https://developers.google.com/speed/docs/insights/MinifyResources)
that will insert semicolons as appropriate when it processes our code. And
lately, it's becoming more popular to compile ECMAScript 6 to ES5 (the
JavaScript that most browsers work in) using a tool like [Babel](https://babeljs.io/).
[TypeScript](https://www.typescriptlang.org/) is also growing in popularity.

All of this is to say that the long-running semicolon debate in JavaScript
is largely overblown at this point. Remember to use semicolons to separate
statements that occur on a single line; otherwise, follow the conventions of
your team.

## Truthy and Falsey Values

We make a lot of assumptions when we write computer programs. In order to make
the right assumptions, we need to understand what values in our program evaluate
to `truthy` values and which evaluate to `falsey` values.

Truthy values:

```javascript
'all non-empty strings';

'all number strings'; // for example '0', '5', '0.2', '-3.14'

[]; // an empty array

{}; // an empty object

1; // any non-zero number
```

Falsey values:

```javascript
0; // the number zero

'';  // an empty string

NaN;

null;

undefined;
```

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/js-basics-readme' title='Intro to JavaScript'>Intro to JavaScript</a> on Learn.co and start learning to code for free.</p>
