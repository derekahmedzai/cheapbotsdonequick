# Creating image bots using SVG and Tracery

To create images we need to use SVG. CBDQ takes a screenshot of the SVG image and creates a JPG which it uploads to Twitter.

Using SVG is as simple as adding `{svg <svg>YOUR SVG CODE</svg>}` to your text.

You can paste the following examples into CBDQ and they should just work.

## The most basic example:
> {
  "origin": "Here is some SVG: {svg <svg xmlns=\\"http://www.w3.org/2000/svg\" xmlns:xlink=\\"http://www.w3.org/1999/xlink\" width=\\"1024\\" height=\\"512\\"><\/svg>}"
}

Things to note: you need to escape any double quotes (so `"` becomes `\"`) and you need to define the width and height of the image. I think you can use any size you like, but I usually use 1024x512 pixels as it shows up complete and uncropped in the Twitter and Tweetdeck timelines.

## Embed an image
To include an image use the `<image>` SVG tag. You don't need to define the width or height but it's helpful. You can host the images anywhere - I use Dropbox a lot.
> {
  "origin": "*any text / link you like* {svg <svg xmlns=\\"http://www.w3.org/2000/svg\" xmlns:xlink=\\"http://www.w3.org/1999/xlink\" width=\\"*width*\\" height=\\"*height*\\"><image width=\\"*width*\\" height=\\"*height*\\" xlink:href=\\"*path to your image*\\" /><\/svg>}"
}

Here's an example. I've set the width and height of both the SVG object and the image to 512x512.
> {
  "origin": "nonsensical infographics http://www.chadhagen.com/nonsensical-infographics {svg <svg xmlns=\\"http://www.w3.org/2000/svg\" xmlns:xlink=\\"http://www.w3.org/1999/xlink\" width=\\"512\\" height=\\"512\\"><image width=\\"512\\" height=\\"512\\" xlink:href=\\"https://pbs.twimg.com/media/Ch8jRkUWwAAaSlE.jpg:large\" /><\/svg>}"
}

Here's what that looks like:

<img src="https://www.dropbox.com/s/ltcj5f9kkj3az1e/2017-06-16_23-59-25.png?raw=1" width="45%" />

It's all Tracery, so you can put symbols anywhere you like. This example loads a randomly selected image:
> {
  "origin": "*over the garden wall* {svg <svg xmlns=\\"http://www.w3.org/2000/svg\" xmlns:xlink=\\"http://www.w3.org/1999/xlink\" width=\\"*540*\\" height=\\"*380*\\"><image width=\\"*540*\\" height=\\"*380*\\" xlink:href=\\"*#image#*\\" /><\/svg>}",
  "image": ["https://typeset-beta.imgix.net/rehost%2F2016%2F9%2F13%2F99d6595b-3e04-44f1-9fc4-fde9852eb51f.jpg", "http://deadshirt.net/wp-content/uploads/2014/11/1.jpg"]
}

Here's what that looks like:

<img src="https://www.dropbox.com/s/sotpa2z0cq0r61k/2017-06-16_23-45-18.png?raw=1" width="45%" /> <img src="https://www.dropbox.com/s/v4xi3iu3buzc4zr/2017-06-16_23-42-54.png?raw=1" width="45%" />

