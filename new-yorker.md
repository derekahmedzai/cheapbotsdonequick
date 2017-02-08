# Make your own New Yorker cartoon Twitter bot

Yes, you too can make a bot that spews out pictures like these:

<a href="https://twitter.com/time4gametheory/status/827690849245003776"><img src="https://pbs.twimg.com/media/C3yMcGQWAAIqH7i.jpg" alt="Guys. It's time for some game theory." width="45%" /></a>
<a href="https://twitter.com/time4gametheory/status/828868628988755970"><img src="https://pbs.twimg.com/media/C4C7n8kWAAA5dJJ.jpg" alt="Guys. It's time for some game theory." width="45%" /></a>

## 1. Create a Twitter account

Or if you already have one, you can use that.

## 2. Create a Cheap Bots, Done Quick! bot

Go to [Cheap Bots, Done Quick!](http://cheapbotsdonequick.com/) and click the "Sign in with Twitter" button

## 3. Paste this JSON / Tracery code
```javascript
{
 "ABOUT": "this bot tweets a random New Yorker cartoon and add the words 'Guys. It's time for some game theory' at the bottom."
,"MADE BY": "@derekahmedzai"
,"NOTES": "uses New Yorker's random cartoon API to get the image. CBDQ can't use that directly as it is JSON, so created a @Gomixme app to expose the image to CBDQ. The source for that is at https://gomix.com/#!/project/new-yorker-cartoon-url"
,"origin": "#guysitstimeforsomegametheory#"
,"guysitstimeforsomegametheory": "#text# #hashtag##svg#"
,"svg": "{svg <svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"1024\" height=\"512\" style=\"position: relative; background: white;\"><image x=\"0\" y=\"0\" width=\"1024\" height=\"482\" xlink:href=\"#new_yorker_image#\" id=\"img\" />#caption#</svg>}"
,"new_yorker_image": "https://new-yorker-cartoon-url.gomix.me/image"
,"caption" : "<foreignObject  x='0' y='0' width='1024' height='512'><p xmlns=\"http://www.w3.org/1999/xhtml\"><p style='position: absolute; left: 0px; bottom: 10px; width: 1024px; line-height: 1; margin: 0; padding: 0; text-align: center; font-size:20px; font-weight: normal; color:rgba(0, 0, 0, 0.9); font-family:\"Georgia\"; font-style: italic;'>#text#</p></p></foreignObject>"
,"text": "\"Guys. It's time for some game theory.\""
,"hashtag": ["\\#gametheory", "\\#thread", ""]
}
```

## 4. Do a test tweet

Click the "Tweet" button. If you don't like the current picture, click the reload button until you find one you do like.

## 5. Set a schedule

Choose how often to tweet. Once an hour is plenty!

## 6. Save it

Don't forget to save it! And share the code if you are feeling generous :)

## 7. Make it yours

### Easy
* change the text by editing the "text" value. Some characters, like quotes and hashtags need to be escaped (with a slash `\`)
* change the hashtags by editing the "hashtag" value
* change the image by editing the "new_yorker_image" value

### Advanced
* use SVG filters to change the image - colour, blur, flip it
* change the font. You can use system fonts or even include Google webfonts

## 8. Common problems

* Twitter might lock your account for "unusual tweeting". Add your phone number to unlock your account - you can remove your phone number from your account after unlocking it
