# 🎁 How to Customize Your Birthday Page

## Quick Customization Guide

### 1. **Change the Messages**
Edit `index.html` and modify the messages inside the `<div id="code">` section:

```html
<span class="say">My beautiful wife 💞</span><br>
<span class="say">Happy Birthday 🎈</span><br>
<span class="say">May God bless you 🍀</span><br>
<span class="say">And give u many happiness 💕</span><br>
<span class="say">I loved you ❤️</span><br>
<span class="say">And I will always love u 🥺 ❤️</span><br>
<span class="say">Hope u have a great day today ❤️😘</span><br>
```

### 2. **Change the Starting Date (for the counter)**
In `index.html`, find this line in the script:
```javascript
timeElapse(new Date(2020, 0, 1));
```

Change it to your date:
```javascript
timeElapse(new Date(2020, 5, 15)); // June 15, 2020 (month is 0-indexed)
```

### 3. **Add Background Music**
- Place your MP3 file in the root folder and name it `aud.mp3`
- The music will play when the user clicks on the heart

### 4. **Change Colors**
Edit `file/default.css` and find:
```css
body {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
}
```

Popular color gradients:
```css
/* Sunset */
background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);

/* Ocean */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* Forest */
background: linear-gradient(135deg, #134e5e 0%, #71b280 100%);

/* Fire */
background: linear-gradient(135deg, #ff6b6b 0%, #feca57 100%);
```

### 5. **Change the Page Title**
Edit `index.html`:
```html
<title>🎂 Happy Birthday My Love 💖</title>
```

Change to:
```html
<title>🎂 Happy Birthday [Name] 💖</title>
```

### 6. **Customize Text Colors**
In `file/default.css`, find color values:
```css
#code {
  color: #e0f7ff; /* Light cyan color */
}

.say {
  border-left: 4px solid #ff6b9d; /* Border color */
  background: rgba(255, 255, 255, 0.1); /* Background transparency */
}
```

### 7. **Add More Messages**
Simply add more `<span class="say">` elements in the HTML:
```html
<span class="say">This is a new message 💝</span><br>
<span class="say">And another one! 🎉</span><br>
```

### 8. **Slow Down or Speed Up Animations**
In `file/functions.js`, find:
```javascript
}, 75); // 75 milliseconds between character displays
```

- Lower number = Faster typing
- Higher number = Slower typing

### 9. **Change Canvas Size**
In `index.html`, update:
```html
<canvas id="canvas" width="1100" height="680"></canvas>
```

However, the CSS now handles responsive sizing automatically.

### 10. **Customize the Clock Counter**
The counter shows days, hours, minutes, and seconds since a starting date.
In `file/functions.js`:
```javascript
function timeElapse(date){
    // The counter will calculate time from 'date' to now
}
```

Change the date passed to this function in `index.html`:
```javascript
timeElapse(new Date(2020, 0, 1)); // Change this!
```

---

## Advanced Customization

### Change the Heart Tree Colors
In `index.html`, find the `opts` object around line 60:
```javascript
var opts = {
    seed: {
        x: width / 2 - 20,
        color: "rgb(190, 26, 37)", // Seed color
        scale: 2
    },
    // ...
}
```

Change the RGB color:
- `rgb(255, 0, 0)` = Red
- `rgb(255, 192, 203)` = Pink
- `rgb(0, 0, 255)` = Blue
- `rgb(255, 255, 0)` = Yellow

### Modify Branch Lengths and Positions
The `branch` array in `opts` controls the tree shape. Each array represents a branch:
```javascript
[535, 680, 570, 250, 500, 200, 30, 100, [...]]
       ↑    ↑    ↑    ↑   ↑    ↑   ↑   ↑
      x1   y1   x2   y2  x3   y3  radius length
```

### Add More Flowers
Change the bloom settings:
```javascript
bloom: {
    num: 700,    // Number of flowers (increase for more)
    width: 1080, // Bloom area width
    height: 650, // Bloom area height
}
```

---

## Mobile Customization

The site is now responsive! But if you want to customize mobile-specific styles:

Edit `file/default.css` and find the media queries:

```css
@media (max-width: 768px) {
    /* Tablet adjustments */
}

@media (max-width: 480px) {
    /* Mobile adjustments */
}
```

---

## Testing Your Changes

1. **Save all files** (no build process needed!)
2. **Open index.html** in your browser
3. **Refresh** (Ctrl+R or Cmd+R) to see changes
4. **Test on mobile** by resizing your browser or using device emulation (F12)

---

## Emoji Reference

Popular emojis for birthday messages:
- 🎂 Birthday cake
- 🎉 Confetti
- 🎈 Balloon
- 💖 Love heart
- 🥳 Party face
- 🌹 Rose
- ❤️ Red heart
- 💕 Two hearts
- 🎁 Gift
- ⭐ Star
- 🌟 Glowing star
- 💝 Heart with ribbon
- 🍀 Four-leaf clover
- 👑 Crown
- 💐 Bouquet

---

## Need Help?

### Common Issues:

**Q: Music doesn't play**  
A: Make sure the file is named exactly `aud.mp3` and is in the root folder

**Q: Colors look different**  
A: Clear your browser cache (Ctrl+Shift+Delete) and refresh

**Q: Text appears at wrong position**  
A: Don't change the `#text` positioning values in CSS, they're optimized

**Q: Canvas not displaying**  
A: Use a modern browser (Chrome, Firefox, Safari, Edge)

---

## File Structure

```
Happay-Day-main/
├── index.html              (Main file - customize here)
├── aud.mp3                 (Add your music file here)
├── README.md               (Project description)
├── IMPROVEMENTS.md         (What was fixed)
├── CUSTOMIZATION.md        (This file)
└── file/
    ├── default.css         (Styling - customize colors here)
    ├── love.js             (Canvas drawing logic)
    ├── functions.js        (Clock and animations)
    ├── jquery.min.js       (Library)
    ├── jscex*.js           (Libraries)
    └── other files
```

---

**Enjoy creating your personalized birthday page! 🎂💖**
