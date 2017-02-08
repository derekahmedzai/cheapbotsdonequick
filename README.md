# Making twitter bots using Cheap Bots Done Quick

[Cheap Bots, Done Quick](http://cheapbotsdonequick.com/) is a platform for generative Twitter bots.

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

Here's one of the best Cheap Bots Done Quick tutorials - http://barrl.net/2767

Text is great, but the reason that I love Cheap Bots Done Quick is that you can define images in SVG that are part of the tweet.

<img src="https://pbs.twimg.com/media/C4CyQpaXAAAAssZ.jpg:large" width="20%" />
<img src="https://pbs.twimg.com/media/C4JHhlqWYAA2s6N.png:large" width="20%" />
<img src="https://pbs.twimg.com/media/C4FfBLVWQAA0DxE.jpg:large" width="20%" />
<img src="https://pbs.twimg.com/media/C4FuJerW8AA4jOn.jpg:large" width="20%" />

## Make your own New Yorker cartoon Twitter bot

### Steps
* Create a Twitter account
* Create a Cheap Bots Done Quick app
* Copy and edit this Tracery code
* Make it yours
  - Colours, fonts, text, images
