# Copilot Instructions for Portfolio Website

## Project Overview
This is a personal portfolio website built using the Dimension template by HTML5 UP. The site features a modern, single-page design with modal-based navigation and interactive animations.

## Architecture & Structure
- `index.html`: Main entry point with modal-based "pages" structure
- `assets/`: Contains all static resources
  - `css/`: Stylesheet files including Font Awesome integration
  - `js/`: JavaScript modules for functionality
  - `sass/`: Source SCSS files organized by feature
  - `webfonts/`: Font resources

## Key Patterns & Conventions

### Modal Page Structure
- Each section is an `<article>` within `#main` div
- Navigation uses href anchors (e.g., `#intro`, `#certificate`)
- Modal content triggered by navigation uses CSS classes for transitions

### JavaScript Architecture (`assets/js/main.js`)
- Uses jQuery for DOM manipulation
- Implements responsive breakpoints system:
```javascript
breakpoints({
    xlarge:   [ '1281px',  '1680px' ],
    large:    [ '981px',   '1280px' ],
    medium:   [ '737px',   '980px'  ],
    small:    [ '481px',   '736px'  ],
    xsmall:   [ '361px',   '480px'  ],
    xxsmall:  [ null,      '360px'  ]
});
```

### CSS/SASS Structure
- Base styles in `sass/base/`
- Component-specific styles in `sass/components/`
- Layout modules in `sass/layout/`
- Library configurations in `sass/libs/`

### Animation Patterns
- Uses CSS classes for transitions:
  - `.fading-text`: Text fade-in effects
  - `.slide-in-text-left-to-right`, `.slide-in-text-right-to-left`: Directional slide animations
  - `.is-preload`: Initial page load state

## Development Workflow
1. Edit HTML content in `index.html`
2. Style modifications:
   - Edit SASS files in `assets/sass/`
   - Compile to CSS (requires SASS compiler)
3. JavaScript enhancements go in `assets/js/main.js`

## External Dependencies
- jQuery for DOM manipulation and effects
- Font Awesome for icons (v5+)
- Breakpoints.js for responsive design handling
- Responsive Tools (from github.com/ajlkn/responsive-tools)