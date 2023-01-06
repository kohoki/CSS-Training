# CSS-Training

Collecting information to help me expand my knowledge.
Based on the best of my knowledge and experience.

## 1 Static Positioning

![Picture-of-1Round](https://github.com/kohoki/CSS-Training/blob/8c15f65797b72de0e3bc01f4052c57d8b063124d/1round/1round.png)

## 2 Relative Positioning

![Picture-of-2Round](https://github.com/kohoki/CSS-Training/blob/bf42cb7a09221b8d13c9ff1f29b79678f30572f6/2round/2round.png)

### 2.1 Absolute Positioning

![Picture-of-21Round](https://github.com/kohoki/CSS-Training/blob/00d9dd1a3b2b7d4cf2ca9100a28e3b8e060a5e50/2.1round/21round.png)

## 3 Dark Art of Centering Elements

```
body {
text-align: center; // centres text and all inline block elements
}

// but - if i would change the width of the h1 - this element would not be in the middle anymore
// then the first friend would be margin
h1 {
width: 10%; // now it is left
margin: 0 auto 0 auto; // (top|0| right|auto| bottom|0| left|auto|) now it is in the middle :-)
margin: 0 auto; // the same result
}
```

## 4 Image Size

The goal is to have the same size of the pictures. Each picture has a different starting size.

![Picture-of-4Round](https://github.com/kohoki/CSS-Training/blob/e018c79b7ee62a6bb33e337aa7f70fabbe9cf958/4round/2.png)

```
body {
  text-align: center;
}
.topContainer {
  margin: auto;
  height: 100px;
  width: 200px;
}

.topContainer img {
  width: 25%;           // Good to know. The changed width refers in relation to the parent. This would be the div. Consequently, all images have the same size.
}
```

### 4.1 float arround image

Without flexbox or grit arrangement of images and text.

![Picture-of-4.1Round](https://github.com/kohoki/CSS-Training/blob/e66addf55947b7e47bc63f722779ebed90783187/4.1round/1.png)

```
div img {
  padding: 20px 0 20px 20px;
  width: 25%;
  float: left;      // This allows the other elements to arrange themselves around the image in that case.
}
p {
  clear: left;      // It is more or less the anti float. | This means that the text is no longer arranged next to the image.
  line-height: 1.5rem;
}

```

## Fonts

```
font-family: serif; //have small lines at the ends of the letters called serifs
font-family: sans-serif; // while sans-serif fonts have no serifs and are often used in digital applications
font-family: monospace; // all letters have the same width - mostly code editors and terminal emulators
```

#### Fonts fallback

font-family: 'Roboto', sans-serif;

#### "Web Safe" Fonts for HTML and CSS

check:
https://www.cssfontstack.com/

#### If you want everyone to have your font:

https://fonts.google.com/

##### As an example

To embed a font, copy the code into the `<head>` of your html

```
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Roboto&family=Sacramento&display=swap" rel="stylesheet">
```

CSS rules to specify families

```
font-family: 'Roboto', sans-serif;
font-family: 'Sacramento', cursive;
```

#### Font size

```
font-size: 16px; // 16px = 100% | 90px/16 = 5,625 -> 562,5%
font-size: 1em;  // 16px = 100% = 1em | 90px/16 = 5,625em
```

##### Good to know

px is static
em + % is dynamic | better for people with limitations - because you can determine the size yourself in the browser
but:

```

body {
    font-size: 2em;
}
h1 {
    font-size: 4em; // --> the result is 6em - 2em from parent + 4em from child (the same with body {font-size: 200%})
}

// best way (seems to be)

h1 {
    font-size: 4rem; --> it ignores the parent - same power like em + extra feature of relative :-)
}

```
