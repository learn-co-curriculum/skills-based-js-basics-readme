# Intro to JavaScript

JavaScript is the de facto language of the internet. It's a tool that, once
mastered, will allow you to interact with users via apps in fun and
interesting ways.

In technobabble, JavaScript is a dynamic, untyped, and interpreted programming
language; it is prototype-based and supports both object-oriented and functional
approaches. What all this means will become more apparent in lessons and through
exposure to the language. But here are the basics.

## Objectives
+ Write your first JavaScript code!

## The Console

The best, possibly most powerful thing about JavaScript is that all modern
browsers know how to run it. In fact, your browser runs a JavaScript sandbox
when you open up the console.

To open up your browser's console from Chrome, type `cmd` + `option` + `j`.
From Firefox, type `cmd` + `option` + `k`. From Safari, you'll first need
[to enable the Web Inspector](https://developer.apple.com/library/mac/documentation/AppleApplications/Conceptual/Safari_Developer_Guide/GettingStarted/GettingStarted.html);
then you can press `cmd` + `option` + `c`. (Windows/Linux users, use `ctrl`
instead of `cmd` if you need to.)

Alternatively, open up Chrome and on any tab (even a blank one) right click and
select `Inspect` from the dropdown. From there, select the `console` tab:

![console](https://s3.amazonaws.com/learn-verified/console.png)

The white space below is your console, a sandbox where you can enter and execute
any JavaScript code you want.

![Executing JavaScript in Console](https://s3.amazonaws.com/learn-verified/exectuing-js-in-console.png)

With your console open, enter:

```javascript
console.log("hello world")
```

You did it! You just wrote some JavaScript!

![hooray](http://i.giphy.com/3ornk5Sou1XMaL44bS.gif)

You should see "hello world" followed by `undefined`. `undefined` is the value
that the `console.log()` function returns.

`console.log()` is, as you probably noted, a function that prints its arguments
to the `console` (that little sandbox-y window that's now opened in your
browser). (As you might have guessed, "log" is a computer-y way of saying
"print".)

If that all seems a little complicated right now, don't worry — it'll make sense
soon, when we learn about objects, and functions, and arguments...

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/js-basics-readme' title='Intro to JavaScript'>Intro to JavaScript</a> on Learn.co and start learning to code for free.</p>
