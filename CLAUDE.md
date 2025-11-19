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
This repository contains an interactive Christmas card application designed to spread holiday cheer through digital means. The application aims to provide a personalized, engaging experience for recipients.

### Key Features
- Interactive holiday animations
- Personalized greeting messages
- Shareable digital cards
- Responsive design for all devices
- Optional audio/music integration
- Dynamic visual effects

### Target Audience
- End users: Recipients of Christmas greetings
- Developers: Contributors to the codebase
- AI Assistants: Automated development support

---

## Repository Structure

### Directory Layout

```
xmas-card/
├── src/                    # Source code
│   ├── components/         # Reusable UI components
│   ├── assets/            # Images, fonts, audio files
│   ├── styles/            # CSS/styling files
│   ├── scripts/           # JavaScript/TypeScript files
│   ├── utils/             # Utility functions
│   └── config/            # Configuration files
├── public/                # Public assets and HTML
├── tests/                 # Test files
│   ├── unit/             # Unit tests
│   ├── integration/      # Integration tests
│   └── e2e/              # End-to-end tests
├── docs/                  # Additional documentation
├── .github/               # GitHub workflows and templates
├── dist/                  # Build output (gitignored)
├── node_modules/          # Dependencies (gitignored)
├── package.json           # Node.js dependencies
├── README.md              # User-facing documentation
├── CLAUDE.md              # This file - AI assistant guide
└── CONTRIBUTING.md        # Contribution guidelines
```

### Key Files

- **index.html** - Main entry point for the application
- **package.json** - Node.js project configuration and scripts
- **tsconfig.json / jsconfig.json** - TypeScript/JavaScript configuration
- **.gitignore** - Files to exclude from version control
- **vite.config.js / webpack.config.js** - Build tool configuration

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

### Core Technologies
- **HTML5** - Semantic markup
- **CSS3** - Styling and animations
- **JavaScript (ES6+)** - Core functionality
- **TypeScript** - Optional type safety

### Potential Libraries/Frameworks
- **Animation:** GSAP, anime.js, Three.js
- **Build Tools:** Vite, Webpack, Rollup
- **Testing:** Jest, Vitest, Playwright
- **Linting:** ESLint, Prettier
- **Version Control:** Git

### Browser Support
- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile browsers (iOS Safari, Chrome Mobile)
- Graceful degradation for older browsers

---

## Common Tasks

### Setup Development Environment

```bash
# Clone repository
git clone <repository-url>
cd xmas-card

# Install dependencies
npm install

# Start development server
npm run dev

# Run tests
npm test

# Build for production
npm run build
```

### Adding a New Feature

1. Create feature branch: `git checkout -b feature/feature-name`
2. Implement feature following conventions
3. Add tests for new functionality
4. Update documentation if needed
5. Commit changes with descriptive message
6. Push and create pull request

### Adding Dependencies

```bash
# Add production dependency
npm install package-name

# Add development dependency
npm install --save-dev package-name
```

### Running Linters

```bash
# Run ESLint
npm run lint

# Auto-fix linting issues
npm run lint:fix

# Format code with Prettier
npm run format
```

---

## Testing Guidelines

### Test Structure

```javascript
describe('ComponentName', () => {
  beforeEach(() => {
    // Setup
  });

  afterEach(() => {
    // Cleanup
  });

  test('should perform expected behavior', () => {
    // Arrange
    const component = new ComponentName();

    // Act
    const result = component.method();

    // Assert
    expect(result).toBe(expectedValue);
  });
});
```

### Test Coverage

- Aim for 80%+ code coverage
- Test happy paths and edge cases
- Test error handling
- Test accessibility features

### Running Tests

```bash
# Run all tests
npm test

# Run tests in watch mode
npm run test:watch

# Run tests with coverage
npm run test:coverage

# Run specific test file
npm test -- ComponentName.test.js
```

---

## Deployment

### Build Process

```bash
# Production build
npm run build

# Preview production build
npm run preview
```

### Deployment Checklist

- [ ] All tests passing
- [ ] No linting errors
- [ ] Documentation updated
- [ ] Version bumped (if applicable)
- [ ] Build successful
- [ ] Assets optimized
- [ ] Performance tested

### Environment Variables

Configure environment-specific variables:

```bash
# .env.development
VITE_API_URL=http://localhost:3000

# .env.production
VITE_API_URL=https://api.production.com
```

---

## Troubleshooting

### Common Issues

**Build Fails:**
- Clear cache: `npm run clean`
- Reinstall dependencies: `rm -rf node_modules && npm install`
- Check Node version compatibility

**Tests Failing:**
- Ensure test environment is set up correctly
- Check for async issues (missing awaits)
- Verify test data and mocks

**Animations Not Working:**
- Check browser compatibility
- Verify CSS/JS is loaded correctly
- Check console for errors

### Debug Mode

Enable debug logging:
```javascript
localStorage.setItem('debug', 'xmas-card:*');
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
- ❌ Skip tests or test writing
- ❌ Commit commented-out code
- ❌ Hard-code values that should be configurable
- ❌ Ignore console warnings or errors
- ❌ Use deprecated APIs or libraries
- ❌ Make breaking changes without discussion
- ❌ Add dependencies without justification

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
- [ ] Code follows project conventions
- [ ] No console.log statements (use proper logging)
- [ ] No TODO comments without context/ticket
- [ ] Error handling implemented
- [ ] Tests written and passing
- [ ] Documentation updated
- [ ] No unused imports or variables
- [ ] Performance considerations addressed
- [ ] Accessibility requirements met
- [ ] Security best practices followed

### Security Considerations

- Validate all user inputs
- Sanitize data before rendering
- Avoid XSS vulnerabilities
- Use secure dependencies (check npm audit)
- Don't commit secrets or API keys
- Use HTTPS for external resources

### Performance Considerations

- Minimize DOM manipulations
- Use requestAnimationFrame for animations
- Lazy load heavy assets
- Optimize images and media
- Debounce/throttle event handlers
- Use CSS transforms over position changes
- Profile before optimizing

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

### Phase 1: Foundation
- [ ] Set up project structure
- [ ] Configure build tools
- [ ] Implement basic card layout
- [ ] Add initial styling

### Phase 2: Core Features
- [ ] Implement animations
- [ ] Add personalization options
- [ ] Create sharing functionality
- [ ] Add audio integration

### Phase 3: Polish
- [ ] Performance optimization
- [ ] Cross-browser testing
- [ ] Accessibility improvements
- [ ] Documentation completion

### Phase 4: Launch
- [ ] Final testing
- [ ] Production deployment
- [ ] Monitoring setup
- [ ] User feedback collection

---

## Resources

### Documentation Links
- [Project README](./README.md)
- [Contributing Guidelines](./CONTRIBUTING.md)
- [API Documentation](./docs/api.md)

### External References
- [MDN Web Docs](https://developer.mozilla.org/)
- [Web Accessibility Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [JavaScript Best Practices](https://github.com/ryanmcdermott/clean-code-javascript)

### Team Communication
- Issues: Track bugs and feature requests
- Pull Requests: Code review and discussion
- Discussions: General questions and ideas

---

## Changelog

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
