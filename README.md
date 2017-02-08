# Making twitter bots using Cheap Bots Done Quick

[Cheap Bots, Done Quick](http://cheapbotsdonequick.com/) is a platform for generative Twitter bots.

It uses [Tracery](https://github.com/galaxykate/tracery) to generate content from JSON source.

At it's simplest, it turns this:
```
{
  "origin" : "Hello World"
}
```
into this:
```
Hello World
```

Tokens (wrapped with a hash like this `#hash#`) are expanded from this:
```
{
  "origin" : "Hello #planets#",
  "planets" : ["Mercury", "Venus", "Mars", "Earth"],
}
```
into any of these (it picks a value randomly each time it runs):
```
Hello Mercury
Hello Venus
Hello Mars
Hello Earth
```

Text is great, but the reason that I love Cheap Bots Done Quick is that you can define images in SVG that are part of the tweet.

## Make your own New Yorker cartoon Twitter bot

### Steps
* Create a Twitter account
* Create a Cheap Bots Done Quick app
* Copy and edit this Tracery code
* Make it yours
  - Colours, fonts, text, images
