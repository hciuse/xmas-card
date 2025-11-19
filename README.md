# 🎄 Christmas Card

A beautiful, personalized static HTML Christmas card that you can send to friends and family. Features a festive background image and holiday music!

![Christmas Card Preview](https://img.shields.io/badge/Status-Ready%20to%20Use-success)

## ✨ Features

- 🖼️ **Customizable Background** - Add your own festive image
- 🎵 **Holiday Music** - Play your favorite Christmas song
- 📱 **Fully Responsive** - Works on desktop, tablet, and mobile
- ♿ **Accessible** - Keyboard navigation and screen reader support
- 🚀 **No Build Required** - Pure HTML/CSS/JavaScript
- 🌐 **Easy to Share** - Host online or send as files

## 🚀 Quick Start

### Option 1: View Locally

1. **Clone or download** this repository
2. **Add your media files** (see Customization below)
3. **Open `index.html`** in your web browser
4. Done! Your Christmas card is ready to view

### Option 2: Share with Friends

**Method A: Zip and Send**
1. Zip the entire folder
2. Send to friends via email or file sharing
3. They simply unzip and open `index.html`

**Method B: Host Online (Recommended)**
1. Upload to [Netlify Drop](https://app.netlify.com/drop) (drag & drop, free)
2. Get a shareable URL instantly
3. Send the link to friends!

## 🎨 Customization

### 1. Change the Background Image

1. Find or create a festive Christmas image
2. Save it as `background.jpg` in the `assets/images/` folder
3. Or use a different name and update line 58 in `index.html`:
   ```html
   background-image: url('./assets/images/your-image-name.jpg');
   ```

**Tips:**
- Use high-quality images (1920x1080 or larger)
- Keep file size under 1MB for fast loading
- Compress with [TinyPNG](https://tinypng.com/) if needed

**Free Image Sources:**
- [Unsplash](https://unsplash.com/s/photos/christmas)
- [Pexels](https://www.pexels.com/search/christmas/)
- [Pixabay](https://pixabay.com/images/search/christmas/)

### 2. Add Your Music

1. Get your favorite Christmas song (MP3 format recommended)
2. Save it as `music.mp3` in the `assets/audio/` folder
3. Or use a different name and update line 45 in `index.html`:
   ```html
   <source src="./assets/audio/your-song.mp3" type="audio/mpeg">
   ```

**Tips:**
- Keep file size under 5MB
- Ensure you have rights to use the music
- MP3 format has the best browser support

**Free Music Sources:**
- [Free Music Archive](https://freemusicarchive.org/)
- [YouTube Audio Library](https://www.youtube.com/audiolibrary)
- [Incompetech](https://incompetech.com/music/royalty-free/)

### 3. Personalize the Message

Open `index.html` and edit the text:

**Line 19-21** - Main greeting:
```html
<h1 class="card__title">Merry Christmas!</h1>
<p class="card__subtitle">Wishing you joy and happiness</p>
```

**Lines 25-30** - Your message:
```html
<p>
    May your holidays be filled with warmth, laughter, and love.
    [Edit this message to your liking]
</p>
```

**Line 33** - Your signature:
```html
<strong>Your Name</strong>
```

### 4. Customize Colors and Styling

Open `styles.css` and modify the CSS variables at the top (lines 7-13):

```css
:root {
    --primary-red: #c41e3a;      /* Main red color */
    --primary-green: #0f7f3f;    /* Main green color */
    --primary-gold: #ffd700;     /* Accent color */
    --text-dark: #2c3e50;        /* Text color */
    --text-light: #ffffff;       /* Light text */
    --card-bg: rgba(255, 255, 255, 0.95);  /* Card background */
}
```

## 🌐 Hosting & Deployment

### GitHub Pages (Free)

1. Push this repository to GitHub
2. Go to repository Settings → Pages
3. Select source: `main` branch, root directory
4. Your site will be live at: `https://username.github.io/xmas-card/`

### Netlify (Free, Easiest)

**Netlify Drop (No account needed):**
1. Go to [https://app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag and drop your folder
3. Get instant URL!

**Netlify with Git:**
1. Sign up at [Netlify](https://netlify.com)
2. Connect your GitHub repository
3. Deploy settings:
   - Build command: (leave empty)
   - Publish directory: `/` (root)
4. Click Deploy!

### Other Options

- **Vercel** - Similar to Netlify, easy deployment
- **Surge.sh** - Simple command-line deployment
- **Firebase Hosting** - Google's hosting platform
- **Any web hosting** - Just upload all files via FTP

## 📁 File Structure

```
xmas-card/
├── index.html              # Main HTML file (open this!)
├── styles.css              # All the styling
├── README.md               # This file
├── CLAUDE.md               # AI assistant documentation
├── .gitignore              # Git ignore rules
└── assets/
    ├── images/
    │   ├── background.jpg  # Your background image (add this)
    │   └── README.md       # Instructions for images
    └── audio/
        ├── music.mp3       # Your Christmas music (add this)
        └── README.md       # Instructions for audio
```

## 🔧 Browser Compatibility

Works in all modern browsers:
- ✅ Chrome/Edge (v90+)
- ✅ Firefox (v88+)
- ✅ Safari (v14+)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## ♿ Accessibility Features

- Semantic HTML5 structure
- ARIA labels for screen readers
- Keyboard navigation support
- Respects reduced motion preferences
- High contrast mode support
- Color contrast compliant

## 🐛 Troubleshooting

**Background image not showing?**
- Check the file exists in `assets/images/`
- Verify the filename matches in `styles.css` (line 58)
- Open browser console (F12) to check for errors

**Audio not playing?**
- Check the file exists in `assets/audio/`
- Verify the filename matches in `index.html` (line 45)
- Note: Most browsers require clicking "Play Music" button
- Try a different audio format if needed

**Card looks broken?**
- Clear browser cache (Ctrl+F5 or Cmd+Shift+R)
- Ensure `styles.css` is in the same folder as `index.html`
- Check browser console for CSS errors

## 📝 License

This project is free to use for personal purposes. Feel free to customize and share!

## 🎁 Credits

Created with ❤️ for spreading holiday cheer.

---

## 💡 Tips for Best Results

1. **Test First** - View the card in multiple browsers before sharing
2. **Optimize Media** - Compress images and audio for faster loading
3. **Personalize** - Add personal touches to make it special
4. **Mobile Test** - Check how it looks on a phone
5. **Backup** - Keep copies of your customized version

## 🤝 Contributing

Have ideas to improve this Christmas card? Feel free to:
- Open an issue with suggestions
- Submit a pull request with enhancements
- Share your customized versions!

---

**Happy Holidays! 🎄✨🎅**

Made with love for the festive season.
