# 🎄 Christmas Card

A beautiful, personalized static HTML Christmas card that you can send to friends and family. Features a festive background image and holiday music!

![Christmas Card Preview](https://img.shields.io/badge/Status-Ready%20to%20Use-success)

## ✨ Features

- 🖼️ **Customizable Background** - Add your own festive image
- 🎵 **Holiday Music** - Play your favorite Christmas song
- 🎅 **Dancing Elves** - Add photos of faces on animated Christmas elves!
- 🔗 **Personalized URL Links** - Create custom messages via encoded URL parameters ✨ **NEW!**
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

### 3. Add Dancing Elves with Face Photos! 🎅

Make your card extra fun by adding photos of people's faces on dancing Christmas elves!

**Step 1: Add Face Photos**
1. Place face photos in the `assets/images/faces/` folder
2. Supported formats: JPG, PNG, GIF, WebP
3. Recommended: 200x200 to 500x500 pixels, square images work best
4. Keep each file under 200KB

**Step 2: Configure the Elf List**
1. Open `index.html` in a text editor
2. Find the `FACE_IMAGES` array (around line 70)
3. Add your image filenames to the array:
   ```javascript
   const FACE_IMAGES = [
       'mom.jpg',
       'dad.png',
       'sister.jpg',
       'friend.png',
   ];
   ```
4. Save and refresh your browser

**Tips:**
- Use clear, well-lit face photos for best results
- Square headshots work better than full-body photos
- PNG with transparent background looks great!
- Remove background using [Remove.bg](https://www.remove.bg/) (free)
- Add 3-8 faces for the best effect (too many can clutter the screen)

**How It Works:**
- Each face photo appears on a Christmas elf body
- Elves dance and move around the screen
- Each elf has a red Santa hat, green outfit, and festive shoes
- Animations include bouncing, wiggling hats, and kicking legs

**Example folder structure:**
```
assets/images/faces/
├── mom.jpg
├── dad.png
├── sister.jpg
└── friend.png
```

### 4. Personalize the Message

**Option A: Edit the HTML directly**

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

**Option B: Use URL Parameters (Personalized Links!)** ✨ **NEW!**

Create personalized card links where each recipient gets a unique message - and they can't preview the text in the URL because it's encoded!

**How to use:**
1. Open `url-generator.html` in your web browser
2. Fill in your personalized message fields:
   - Card Title (e.g., "Happy Holidays Sarah!")
   - Subtitle (e.g., "Wishing you an amazing 2024")
   - Main Message (your personal message)
   - Signature (your name)
3. Click "🎁 Generate URL"
4. Copy the generated link and share it!

**Example URL:**
```
index.html?msg=eyJ0aXRsZSI6IkhhcHB5IEhvbGlkYXlzISIsInN1YnRpdGxlIjoiVGVzdGluZyB0aGUgZmVhdHVyZSIsIm1lc3NhZ2UiOiJUaGlzIGlzIGEgdGVzdCBvZiB0aGUgVVJMIHBhcmFtZXRlciBlbmNvZGluZy4gSWYgeW91IHNlZSB0aGlzLCBpdCB3b3JrcyEiLCJzaWduYXR1cmUiOiJUaGUgRGV2ZWxvcGVyIn0=
```

**Benefits:**
- ✅ Create personalized cards for different recipients
- ✅ Text is base64-encoded so it can't be easily previewed
- ✅ No need to edit HTML for each person
- ✅ Perfect for hosting one card and sharing multiple personalized links
- ✅ Easy to use with the included URL generator tool

**Tips:**
- You can customize all fields (title, subtitle, message, signature)
- Leave any field blank to use the default text from `index.html`
- The URL generator includes a preview button to test your card
- Works great with GitHub Pages or any hosted version

### 5. Customize Colors and Styling

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

### GitHub Pages (Free) - AUTOMATED! ✨

This repository includes a GitHub Actions workflow that **automatically deploys** to GitHub Pages!

**Setup (One-time):**
1. Push this repository to GitHub
2. Go to repository **Settings** → **Pages**
3. Under "Source", select: **GitHub Actions**
4. That's it! Your site will auto-deploy on every push to `main`

**Your site will be live at:** `https://username.github.io/xmas-card/`

**How it works:**
- Every push to the `main` branch triggers automatic deployment
- You can also manually trigger deployment from the "Actions" tab
- No build process needed - deploys instantly!
- The workflow file is at `.github/workflows/deploy.yml`

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
├── url-generator.html      # URL generator tool for personalized links ✨ NEW
├── styles.css              # All the styling
├── README.md               # This file
├── CLAUDE.md               # AI assistant documentation
├── .gitignore              # Git ignore rules
└── assets/
    ├── images/
    │   ├── background.jpg  # Your background image (add this)
    │   ├── faces/          # Face photos for dancing elves
    │   │   ├── mom.jpg     # Example face photos
    │   │   ├── dad.png
    │   │   └── README.md
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
- Verify the filename matches in `index.html` (line 51)
- Note: Most browsers require clicking "Play Music" button
- Try a different audio format if needed

**Elves not appearing?**
- Make sure you added filenames to the `FACE_IMAGES` array in `index.html`
- Check that face photos exist in `assets/images/faces/` folder
- Verify filenames match exactly (including extensions)
- Open browser console (F12) to check for errors
- Check the console message: "Created X dancing elves!"

**Card looks broken?**
- Clear browser cache (Ctrl+F5 or Cmd+Shift+R)
- Ensure `styles.css` is in the same folder as `index.html`
- Check browser console for CSS errors

**URL parameter not working?**
- Check that the URL includes `?msg=` followed by the encoded text
- Verify the base64 encoding is valid (use the `url-generator.html` tool)
- Open browser console (F12) to see any decoding errors
- Make sure you're using the full URL including the parameter
- Test the URL in a private/incognito window to rule out caching issues

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
