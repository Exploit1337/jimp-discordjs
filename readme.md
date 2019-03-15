# Jimp Guide for Discord.js #

### Installation ###
- - - -
```
npm i jimp
```
It is installed using Node and npm.




### What I will show how to do ###
- - - -
- How to write text onto images
- How to add an image over another one
- How to use jimp functions




### Getting Started ###
- - - -
To first use jimp, we have to declare it.
```javascript
var jimp = require('jimp');
```




### Reading Images / Loading Fonts ###
- - - -
```javascript
jimp.loadFont()
```

```javascript
jimp.read()
```

### Usage ###
- - - -
```javascript
let font = await jimp.loadFont(font)
let imagecard = await jimp.read('link')
```
Obviously, the name of these variables can be edited to what you want.

### Examples ###
- - - - 
```javascript
let font = await jimp.loadFont(jimp.FONT_SANS_32_BLACK) // We load one of the default jimp fonts.
let welcome = await jimp.read('https://static-cdn.jtvnw.net/jtv_user_pictures/e91a3dcf-c15a-441a-b369-996922364cdc-profile_image-300x300.png') // We read the image from the link we supplied 
```

### Fonts ###
- - - -
Here are the default fonts supplied by Jimp
```javascript
Jimp.FONT_SANS_8_BLACK; // Open Sans, 8px, black
Jimp.FONT_SANS_10_BLACK; // Open Sans, 10px, black
Jimp.FONT_SANS_12_BLACK; // Open Sans, 12px, black
Jimp.FONT_SANS_14_BLACK; // Open Sans, 14px, black
Jimp.FONT_SANS_16_BLACK; // Open Sans, 16px, black
Jimp.FONT_SANS_32_BLACK; // Open Sans, 32px, black
Jimp.FONT_SANS_64_BLACK; // Open Sans, 64px, black
Jimp.FONT_SANS_128_BLACK; // Open Sans, 128px, black
Jimp.FONT_SANS_8_WHITE; // Open Sans, 8px, white
Jimp.FONT_SANS_16_WHITE; // Open Sans, 16px, white
Jimp.FONT_SANS_32_WHITE; // Open Sans, 32px, white
Jimp.FONT_SANS_64_WHITE; // Open Sans, 64px, white
Jimp.FONT_SANS_128_WHITE; // Open Sans, 128px, white
```

### Writing on an image ###
- - - -
This is most likely going to be the most used thing jimp offers
```javascript
jimp.print()
```

### Usage ###
- - - -
```javascript
jimp.print(font, x, y, 'print message')
```

### Example ###
- - - -
```javascript
let font = await jimp.loadFont(jimp.FONT_SANS_32_BLACK) 
let welcome = await jimp.read('https://s23932.pcdn.co/wp-content/uploads/2016/06/cotton-Canvas-Painting-for-Beginners-060116.jpg') 
welcome.print(font, 20, 20, 'hello') //We print hello on the image we declared as "welcome"
```

### Putting an image over another image ###
- - - -
To put an image over another image you have to use jimps composite function
```javascript
jimp.composite()
```

### Usage ###
- - - -
```js
jimp.composite(image we declared, x, y)
```
