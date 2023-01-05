# CSS-Training

Collecting information to help me expand my knowledge.
Based on the best of my knowledge and experience.

## 1 Round (Static Positioning)

![Picture-of-1Round](https://github.com/kohoki/CSS-Training/blob/8c15f65797b72de0e3bc01f4052c57d8b063124d/1round/1round.png)

## 2 Round (Relative Positioning)

![Picture-of-2Round](https://github.com/kohoki/CSS-Training/blob/bf42cb7a09221b8d13c9ff1f29b79678f30572f6/2round/2round.png)

### 2.1 Round (Absolute Positioning)

![Picture-of-21Round](https://github.com/kohoki/CSS-Training/blob/00d9dd1a3b2b7d4cf2ca9100a28e3b8e060a5e50/2.1round/21round.png)

### 3 Round (Dark Art of Centering Elements)

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

### (Fonts)

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

As an example
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
