# Creating image bots using SVG and Tracery

To create images we need to use SVG. CBDQ takes a screenshot of the SVG image and creates a JPG which it uploads to Twitter.

Using SVG is as simple as adding `{svg <YOUR SVG CODE>}` to your text.

You can paste the following examples into CBDQ and they should just work.

## The most basic example:
> {
  "origin": "Here is some SVG: {svg <svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" width=\"1024\" height=\"512\"></svg>}"
}

Things to note: you need to escape any double quotes (like `\"`) and you need to define the width and height of the image. I think you can use any size you like, but I usually use 1024x512 pixels as it shows up complete and uncropped in the Twitter and Tweetdeck timelines.

## Just an image
To include an image use the `<image>` SVG tag. You don't need to define the width or height but it's helpful.
> {
  "origin": "*any text / link you like* {svg <svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" width=\"*width*\" height=\"*height*\"><image width=\"*width*\" height=\"*height*\" xlink:href=\"*path to your image*\" /></svg>}"
}

### Example of an image:
I've set the width and height of both the SVG object and the image to 512x512.
> {
  "origin": "*nonsensical infographics - http://www.chadhagen.com/nonsensical-infographics* {svg <svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" width=\"*512*\" height=\"*512*\"><image width=\"*512*\" height=\"*512*\" xlink:href=\"*https://pbs.twimg.com/media/Ch8jRkUWwAAaSlE.jpg:large*\" /></svg>}"
}

It's all Tracery, so you can put symbols anywhere you like. This example loads a randomly selected image:
> {
  "origin": "*nonsensical infographics - http://www.chadhagen.com/nonsensical-infographics* {svg <svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" width=\"*512*\" height=\"*512*\"><image width=\"*512*\" height=\"*512*\" xlink:href=\"*#image#*\" /></svg>}",
  "image": ["https://typeset-beta.imgix.net/rehost%2F2016%2F9%2F13%2F99d6595b-3e04-44f1-9fc4-fde9852eb51f.jpg", "http://deadshirt.net/wp-content/uploads/2014/11/1.jpg"]
}

