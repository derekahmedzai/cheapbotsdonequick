# Making twitter bots using Cheap Bots, Done Quick!

* [What is it](#what-is-it)
* [SVG and dynamic content](#svg-and-dynamic-content)
* [Image twitter bot tutorials](#image-twitter-bot-tutorials)

## What is it?
[Cheap Bots, Done Quick!](http://cheapbotsdonequick.com/) is a platform for generative Twitter bots.

It uses [Tracery](https://github.com/galaxykate/tracery) to generate content from JSON source.

At it's simplest, it turns this:
```javascript
{
  "origin" : "Hello World"
}
```
into this:
```
Hello World
```

Tokens (wrapped with a hash like `#this#`) are expanded from this:
```javascript
{
  "origin" : "Hello #planets#",
  "planets" : ["Mercury", "Venus", "Mars", "Earth"]
}
```
into any of these (it picks a value randomly each time it runs):
```
Hello Mercury
Hello Venus
Hello Mars
Hello Earth
```

Here are a couple of good Cheap Bots Done Quick tutorials
https://github.com/codekitchensd/2016-03-24-twitterbots
http://barrl.net/2767

## SVG and dynamic content
Now plain text tweets are great, but the reason that I love Cheap Bots Done Quick is that you can create and tweet images using SVG.
Also, you can create dynamic content using Javascript in SVG - for example, writing the date, or loading external content.

Here are a few bots that use SVG to create random images

[@sadkeanubot](https:/twitter.com/sadkeanubot) | [@badphotoquality](https:/twitter.com/badphotoquality) | [@time4gametheory](https:/twitter.com/time4gametheory) | [@trumptaxbot](https:/twitter.com/trumptaxbot)
-------------|------------------|------------------|-----------------
<a href="https://twitter.com/sadkeanubot"><img src="https://pbs.twimg.com/media/C4CyQpaXAAAAssZ.jpg:large" /></a> | <a href="https://twitter.com/badphotoquality"><img src="https://pbs.twimg.com/media/C4FfBLVWQAA0DxE.jpg:large" /></a> | <a href="https://twitter.com/time4gametheory"><img src="https://pbs.twimg.com/media/C4FuJerW8AA4jOn.jpg:large" /></a> | <a href="https://twitter.com/trumptaxbot"><img src="https://pbs.twimg.com/media/C4dz8HsWQAE4tXl.jpg:large" /></a>
places a pic of Sad Keanu on a random photo of a chair|applies blur or posterise filter to worsen a photo and overlays the date|overlays the "Guys, it's time..." text on a random New Yorker cartoon|calculates how much tax payers are paying for Trump's personal life
[view the source](http://cheapbotsdonequick.com/source/sadkeanubot) | [view the source](http://cheapbotsdonequick.com/source/badphotoquality) | [view the source](http://cheapbotsdonequick.com/source/time4gametheory) | [view the source](http://cheapbotsdonequick.com/source/trumptaxbot)

## Image twitter bot tutorials
* [Make your own New Yorker cartoon Twitter bot](https://github.com/derekahmedzai/cheapbotsdonequick/blob/master/new-yorker.md)
