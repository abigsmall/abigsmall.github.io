---
layout: post
title:  "Things that have tripped me up while writing JavaScript"
date:   2015-09-17 09:06:46:00 -0800
categories: javascript
---
Some common mistakes I’ve made that could’ve been relatively easily avoided.

Many of these would probably not be a problem if I changed the settings in the text editor that I use. Actually, a better blog post than this one would be highlighting useful text editor settings/plug-ins. But I have a deadline so ¯\\\\\\_(ツ)\\_/¯.

## Not saving your files
You make some changes to your code, refresh your browser or run the code in your terminal or wherever, and then... nothing. Nothing changes. ?!?!? You look over your code again, furiously, scanning over each line, character by character. After having looked over your code for the umpteenth time, all you’re left with is a satisfaction at your code’s pristine logic and an intense bewilderment at why your code’s beauty is not being represented in the real world. After several minutes of this, you realize that you didn’t save your changes. Yeah, so save your changes.

## Forgetting a `return` statement
Console doesn’t show any errors and yet I don’t see what I expect. Could be a case of simply forgetting a `return` statement.

Let’s say the below code is in a function, and `anotherFunction` is a function that returns something. To be more specific, `anotherFunction` is a pure function that returns a value and doesn’t have a side effect. That is, the entire purpose of using `anotherFunction` is to return the value that it returns:
```
if (something) {
   anotherFunction();
 }
```
Yet we forgot to return `anotherFunction`’s value!

```
if (something) {
  return anotherFunction();
}
```
Ahh, much better. I’m not sure if linters can check for this. It would do me some good to do some research. I’ll do some later."