# AGENTS.md - Repository Guidelines for Coding Agents

## Overview
This is a simple HTML game repository containing three browser-based games (Snake, Block Blast, and 2048) with a main index page. All code is vanilla HTML/CSS/JavaScript with no external dependencies or build tools.

## Build/Test Commands
This repository contains static HTML files with no build process or testing framework:
- **Local development**: Open `index.html` directly in a web browser
- **No build commands**: All files are static and self-contained
- **No test commands**: No automated tests are present
- **No linting**: No linting tools are configured

To verify changes:
1. Open the specific game file in a browser (game1.html, game2.html, game3.html)
2. Test the game functionality manually
3. Check that all games are accessible from the main index page

## Code Style Guidelines

### HTML Structure
- Use `<!DOCTYPE html>` declaration
- Set `lang="zh-TW"` or `lang="zh-HK"` for Chinese content
- Include `<meta charset="UTF-8">` and responsive viewport meta tag
- Structure: `<html> -> <head> -> <body>` with proper semantic HTML5 elements

### CSS Conventions
- Use internal `<style>` tags within HTML files (no external CSS files)
- Follow BEM-like naming for classes (e.g., `.game-container`, `.tile`, `.score-box`)
- Use CSS custom properties (variables) for theming with `:root` selector
- Implement responsive design with `@media` queries for mobile devices
- Use flexbox and grid for layouts
- Apply smooth transitions and animations for game interactions

### JavaScript Patterns
- Use modern ES6+ features (classes, arrow functions, const/let)
- Organize code into classes for game logic (e.g., `GameManager`, `Tile`)
- Use `localStorage` for persisting high scores and game state
- Implement proper event handling with `addEventListener`
- Use `requestAnimationFrame` for game loops and animations
- Handle both keyboard and touch events for mobile compatibility

### Naming Conventions
- **Files**: Lowercase with hyphens for separation (e.g., `game1.html`, `index.html`)
- **Classes**: PascalCase for JavaScript classes, kebab-case for CSS classes
- **Variables**: camelCase for JavaScript variables
- **Constants**: UPPER_SNAKE_CASE for configuration constants
- **Functions**: camelCase with descriptive names

### Code Organization
- Place CSS in `<head>` section
- Place JavaScript at end of `<body>` before closing tag
- Group related functionality together (game logic, rendering, input handling)
- Use comments to explain complex game mechanics and algorithms
- Maintain consistent indentation (4 spaces preferred)

### Error Handling
- Validate user input for game controls
- Handle edge cases in game logic (boundary checks, collision detection)
- Provide user feedback for invalid actions
- Use try-catch blocks for localStorage operations

### Performance Considerations
- Use CSS transforms instead of changing position properties for animations
- Implement debouncing for rapid input events
- Optimize game loops with proper frame rate management
- Use `will-change` CSS property for animated elements

### Internationalization
- Use Traditional Chinese characters for UI text
- Set appropriate `lang` attributes in HTML
- Consider mobile touch interfaces for accessibility

## File Structure
```
/
├── index.html          # Main game lobby/index page
├── game1.html          # Snake game
├── game2.html          # Block Blast game  
├── game3.html          # 2048 game
├── README.md           # Project documentation
└── AGENTS.md          # This file
```

## Development Workflow
1. Make changes to specific game files as needed
2. Test in browser to verify functionality
3. Ensure responsive design works on mobile devices
4. Check that all games link properly from index.html
5. Update README.md if significant changes are made

## Common Patterns
- **Game initialization**: Create `init()` or constructor methods
- **Game loop**: Use `requestAnimationFrame` with `update()` and `draw()` methods
- **State management**: Use class properties for game state
- **Event handling**: Separate methods for different input types
- **Scoring**: Implement score tracking with localStorage persistence
- **Responsive design**: Use CSS variables and media queries for device compatibility

Remember this is a simple educational game repository - keep code clean, readable, and maintain the existing game mechanics when making improvements or fixes.