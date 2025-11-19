# CLAUDE.md - AI Assistant Guide for xmas-card Repository

**Last Updated:** 2025-11-19
**Repository:** xmas-card
**Purpose:** Interactive Christmas card application

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Repository Structure](#repository-structure)
3. [Development Workflow](#development-workflow)
4. [Key Conventions](#key-conventions)
5. [Technology Stack](#technology-stack)
6. [Common Tasks](#common-tasks)
7. [Testing Guidelines](#testing-guidelines)
8. [Deployment](#deployment)
9. [Troubleshooting](#troubleshooting)
10. [AI Assistant Guidelines](#ai-assistant-guidelines)

---

## Project Overview

### Purpose
This is a **simple static HTML Christmas card** that can be sent to friends. It's a single-page website that displays a festive background image and plays holiday music.

### Key Features
- Static HTML/CSS/JavaScript (no build process required)
- Background image support (customizable by replacing image file)
- MP3 audio playback from assets folder
- Festive holiday greeting message
- Responsive design for viewing on any device
- Easy to customize and share

### Target Audience
- Personal use: Sending holiday greetings to friends and family
- Anyone who wants a simple, customizable digital Christmas card
- AI Assistants: Automated development support

---

## Repository Structure

### Directory Layout

```
xmas-card/
├── assets/                 # Asset files
│   ├── images/            # Background images
│   │   └── background.jpg # Main background image (replace to customize)
│   └── audio/             # Audio files
│       └── music.mp3      # Christmas music (replace to customize)
├── styles.css             # All styling for the card
├── index.html             # Main HTML file (open this in browser)
├── .gitignore             # Files to exclude from version control
├── README.md              # User-facing documentation
└── CLAUDE.md              # This file - AI assistant guide
```

### Key Files

- **index.html** - Main HTML file containing the Christmas card structure
- **styles.css** - All CSS styling and animations
- **assets/images/background.jpg** - Background image (replace this file to change background)
- **assets/audio/music.mp3** - Christmas music (replace this file to change music)
- **.gitignore** - Excludes large media files from git tracking
- **README.md** - Instructions for customizing and using the card

---

## Development Workflow

### Branch Strategy

**Main Branches:**
- `main` - Production-ready code
- `develop` - Integration branch for features
- `feature/*` - Feature development branches
- `bugfix/*` - Bug fix branches
- `claude/*` - AI assistant working branches

**Branch Naming Convention:**
```
feature/description-of-feature
bugfix/issue-number-bug-description
claude/claude-md-[session-id]
```

### Git Workflow

1. **Create Feature Branch**
   ```bash
   git checkout -b feature/new-animation
   ```

2. **Make Changes**
   - Write code following conventions
   - Test thoroughly
   - Commit with clear messages

3. **Commit Guidelines**
   ```bash
   git commit -m "type(scope): brief description"
   ```

   **Types:**
   - `feat` - New feature
   - `fix` - Bug fix
   - `docs` - Documentation changes
   - `style` - Code style changes (formatting)
   - `refactor` - Code refactoring
   - `test` - Adding tests
   - `chore` - Maintenance tasks

4. **Push and Create PR**
   ```bash
   git push -u origin feature/new-animation
   ```

### Code Review Process

- All changes require review before merging
- Automated tests must pass
- Code must follow style guidelines
- Documentation must be updated if needed

---

## Key Conventions

### Code Style

**JavaScript/TypeScript:**
- Use ES6+ syntax
- Prefer `const` over `let`, avoid `var`
- Use arrow functions for callbacks
- Use async/await over promises where possible
- Use descriptive variable names (camelCase)
- Add JSDoc comments for functions

**Example:**
```javascript
/**
 * Generates a personalized greeting message
 * @param {string} recipientName - Name of the card recipient
 * @param {Object} options - Customization options
 * @returns {string} Formatted greeting message
 */
const generateGreeting = (recipientName, options = {}) => {
  const { style = 'formal', includeEmoji = true } = options;
  // Implementation
};
```

**CSS/Styling:**
- Use BEM naming convention for classes
- Organize styles by component
- Use CSS variables for theming
- Mobile-first responsive design
- Prefer flexbox/grid over floats

**Example:**
```css
.card {
  /* Block */
}

.card__header {
  /* Element */
}

.card--festive {
  /* Modifier */
}
```

### File Naming

- **Components:** PascalCase (e.g., `SnowAnimation.js`)
- **Utilities:** camelCase (e.g., `dateFormatter.js`)
- **Styles:** kebab-case (e.g., `card-animation.css`)
- **Tests:** Match source file with `.test` or `.spec` suffix (e.g., `SnowAnimation.test.js`)

### Component Structure

```javascript
// Component header
import { dependency } from 'library';
import './ComponentName.css';

// Constants and configuration
const DEFAULT_CONFIG = {};

// Main component
class ComponentName {
  constructor(options) {
    this.options = { ...DEFAULT_CONFIG, ...options };
    this.init();
  }

  init() {
    // Initialization logic
  }

  // Public methods

  // Private methods (prefix with _)
  _privateMethod() {}
}

export default ComponentName;
```

---

## Technology Stack

### Core Technologies (No Dependencies Required!)
- **HTML5** - Semantic markup for card structure
- **CSS3** - Styling, animations, and responsive design
- **JavaScript (Vanilla)** - Audio controls and interactivity
- **Git** - Version control

### No Build Process
This is a **static website** - no Node.js, npm, or build tools required. Simply open `index.html` in a browser!

### Browser Support
- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile browsers (iOS Safari, Chrome Mobile)
- Works offline once downloaded

---

## Common Tasks

### Setup and View

```bash
# Clone repository
git clone <repository-url>
cd xmas-card

# Open in browser (no build step needed!)
open index.html
# or double-click index.html in file explorer
```

### Customizing the Card

**Change Background Image:**
1. Replace `assets/images/background.jpg` with your own image
2. Keep the same filename or update the path in `index.html`
3. Supported formats: JPG, PNG, GIF, WebP

**Change Music:**
1. Replace `assets/audio/music.mp3` with your own audio file
2. Keep the same filename or update the path in `index.html`
3. Supported formats: MP3, OGG, WAV

**Edit Greeting Message:**
1. Open `index.html` in any text editor
2. Find the greeting text section
3. Edit the message to your liking
4. Save and refresh browser

**Modify Styling:**
1. Open `styles.css` in any text editor
2. Adjust colors, fonts, animations
3. Save and refresh browser

### Sharing Your Card

**Option 1: Direct File Sharing**
- Zip the entire folder and send it
- Recipient opens `index.html` in their browser

**Option 2: Host on Web**
- Upload to GitHub Pages (free)
- Use Netlify Drop (drag & drop, free)
- Use any static hosting service

**Option 3: Screen Recording**
- Record the card playing in browser
- Share as video file

---

## Testing Guidelines

### Manual Testing Checklist

Since this is a simple static site, testing is straightforward:

**Visual Testing:**
- [ ] Background image displays correctly
- [ ] Text is readable against background
- [ ] Animations work smoothly
- [ ] Layout is centered and pleasing
- [ ] Responsive on mobile devices

**Audio Testing:**
- [ ] Music plays when page loads (or on user interaction)
- [ ] Audio controls work (play/pause)
- [ ] Volume control functions properly
- [ ] Audio file loads without errors

**Browser Testing:**
- [ ] Test in Chrome
- [ ] Test in Firefox
- [ ] Test in Safari
- [ ] Test on mobile device
- [ ] Check console for errors (F12 Developer Tools)

**Accessibility Testing:**
- [ ] Can navigate with keyboard
- [ ] Alt text provided for images
- [ ] Sufficient color contrast
- [ ] Works with screen readers

---

## Deployment

### No Build Required!
This is a static HTML site - all files can be deployed as-is.

### Deployment Options

**GitHub Pages (Free):**
```bash
# Enable GitHub Pages in repository settings
# Set source to main branch, root directory
# Your site will be at: https://username.github.io/xmas-card/
```

**Netlify Drop (Free, No Account Needed):**
1. Go to https://app.netlify.com/drop
2. Drag and drop your entire `xmas-card` folder
3. Get instant URL to share

**Netlify with Git (Free):**
1. Connect repository to Netlify
2. No build command needed
3. Publish directory: `/` (root)
4. Auto-deploys on every push

**Other Options:**
- Vercel
- Surge.sh
- Firebase Hosting
- Any web hosting service with FTP

### Pre-Deployment Checklist

- [ ] Test card in multiple browsers
- [ ] Verify background image displays correctly
- [ ] Confirm audio plays properly
- [ ] Check mobile responsiveness
- [ ] Ensure all file paths are relative (not absolute)
- [ ] Test audio file size (keep under 5MB for fast loading)
- [ ] Optimize image file size if needed

---

## Troubleshooting

### Common Issues

**Background Image Not Showing:**
- Check file path in `index.html` matches actual file location
- Verify image file exists in `assets/images/` folder
- Check browser console (F12) for 404 errors
- Ensure file extension matches (jpg vs jpeg vs png)

**Audio Not Playing:**
- Check file path in `index.html` matches actual file location
- Verify audio file exists in `assets/audio/` folder
- Check browser console (F12) for errors
- Note: Some browsers block autoplay - may need user interaction
- Try different audio format (MP3 vs OGG)
- Ensure file isn't corrupted

**Styles Not Applied:**
- Verify `styles.css` is in the same directory as `index.html`
- Check for typos in `<link>` tag
- Clear browser cache (Ctrl+F5 or Cmd+Shift+R)
- Check browser console for CSS errors

**File Paths Broken After Deployment:**
- Use relative paths (e.g., `./assets/images/background.jpg`)
- Don't use absolute paths (e.g., `/Users/name/xmas-card/...`)
- Test locally by opening from different directory

### Debug Tips

**Check Browser Console:**
```
Open Developer Tools: F12 (Windows/Linux) or Cmd+Option+I (Mac)
Look for red error messages
Check Network tab for failed file loads
```

---

## AI Assistant Guidelines

### When Working on This Repository

**DO:**
- ✅ Read this CLAUDE.md file first
- ✅ Follow established conventions and patterns
- ✅ Write tests for new functionality
- ✅ Update documentation when making changes
- ✅ Use TodoWrite tool to track multi-step tasks
- ✅ Make small, focused commits
- ✅ Ask for clarification when requirements are unclear
- ✅ Consider accessibility in all implementations
- ✅ Optimize for performance
- ✅ Handle errors gracefully

**DON'T:**
- ❌ Push to main branch directly
- ❌ Add external dependencies (keep it simple!)
- ❌ Commit commented-out code
- ❌ Use absolute file paths (breaks portability)
- ❌ Ignore console warnings or errors
- ❌ Use deprecated HTML/CSS features
- ❌ Make the project complex (it's meant to be simple)
- ❌ Commit large media files without checking .gitignore

### Task Approach

1. **Understand Requirements**
   - Read the task description carefully
   - Ask clarifying questions if needed
   - Check related issues/PRs

2. **Plan Implementation**
   - Use TodoWrite to track steps
   - Identify affected files
   - Consider edge cases

3. **Implementation**
   - Follow code conventions
   - Write clean, readable code
   - Add appropriate comments
   - Handle errors properly

4. **Testing**
   - Write unit tests
   - Run existing tests
   - Manual testing if needed

5. **Documentation**
   - Update relevant docs
   - Add inline comments for complex logic
   - Update CLAUDE.md if conventions change

6. **Review & Commit**
   - Review your changes
   - Commit with clear messages
   - Push to feature branch
   - Create PR with description

### Code Quality Checklist

Before committing, verify:
- [ ] Code is simple and readable
- [ ] No console.log statements left in code
- [ ] All file paths are relative, not absolute
- [ ] HTML is semantic and valid
- [ ] CSS is organized and commented
- [ ] JavaScript is vanilla (no dependencies)
- [ ] Works in major browsers
- [ ] Tested on both desktop and mobile
- [ ] Accessibility requirements met
- [ ] Documentation updated if needed

### Security Considerations

- No user input in this simple card (minimal security concerns)
- Don't commit personal data or private photos
- If adding external resources, use HTTPS
- Be cautious with any JavaScript added later
- Safe to share - no server-side code or data collection

### Performance Considerations

- Keep background image under 1MB (compress if needed)
- Keep audio file under 5MB for fast loading
- Use CSS animations over JavaScript when possible
- Optimize images with tools like TinyPNG or ImageOptim
- Consider providing thumbnail/preview while assets load
- Test load time on slow connections

### Accessibility Guidelines

- Use semantic HTML
- Provide alt text for images
- Ensure keyboard navigation works
- Maintain color contrast ratios
- Add ARIA labels where needed
- Test with screen readers
- Support reduced motion preferences

---

## Project Milestones

### ✅ Phase 1: Foundation (Complete)
- [x] Create project structure
- [x] Add basic HTML structure
- [x] Set up CSS styling
- [x] Create assets folders

### Phase 2: Core Features (Current)
- [ ] Add background image display
- [ ] Implement audio player
- [ ] Add greeting message
- [ ] Style with festive theme

### Phase 3: Polish
- [ ] Add animations (snowfall, sparkles, etc.)
- [ ] Mobile responsive design
- [ ] Cross-browser testing
- [ ] Performance optimization

### Phase 4: Launch
- [ ] Final testing on multiple devices
- [ ] Deploy to web hosting
- [ ] Create README with instructions
- [ ] Share with friends!

---

## Resources

### Documentation Links
- [Project README](./README.md) - User-facing instructions

### External References
- [MDN HTML Reference](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [MDN CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [MDN JavaScript Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [HTML5 Audio Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio)
- [Web Accessibility Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)

### Inspiration & Resources
- Free Christmas images: [Unsplash](https://unsplash.com/s/photos/christmas), [Pexels](https://www.pexels.com/search/christmas/)
- Free Christmas music: [Free Music Archive](https://freemusicarchive.org/), [YouTube Audio Library](https://www.youtube.com/audiolibrary)
- CSS Animation examples: [Animate.css](https://animate.style/), [CSS-Tricks](https://css-tricks.com/)

---

## Changelog

### Updated with Actual Scope - 2025-11-19
- Updated to reflect static HTML Christmas card project
- Simplified to match no-build, no-dependencies approach
- Added specific instructions for customizing background and audio
- Included deployment options for static sites
- Added troubleshooting for common static site issues

### Template Created - 2025-11-19
- Initial CLAUDE.md structure
- Comprehensive guidelines for AI assistants
- Development workflow documentation
- Code conventions and best practices

---

## Questions or Suggestions?

If you notice this documentation is out of date or have suggestions for improvement:
1. Open an issue with the `documentation` label
2. Submit a PR with proposed changes
3. Discuss in team channels

**Remember:** This file should evolve with the project. Keep it updated!
