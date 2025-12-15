# WordPress with Webpack

A WordPress development setup featuring the Twenty Twenty-One child theme with modern build tools using Webpack, Babel, and Sass.

## Overview

This project provides a customizable WordPress theme development environment with:

- **Twenty Twenty-One Child Theme** with Webpack configuration
- Modern JavaScript transpilation using Babel
- Sass/SCSS compilation
- BrowserSync for live reloading
- Automated asset bundling and optimization

## Project Structure

```
wp-content/
├── themes/
│   ├── twentytwentyone/          # Parent theme
│   └── twentytwentyone-child/    # Child theme with Webpack setup
│       ├── webpack.config.js
│       ├── package.json
│       ├── functions.php
│       ├── assets/
│       │   ├── css/
│       │   └── js/
│       └── dist/                 # Built assets
└── uploads/
```

## Prerequisites

- Node.js (v12 or higher)
- npm or yarn
- WordPress installation
- PHP 7.4 or higher

## Installation

1. Clone this repository:
   ```bash
   git clone <your-repo-url>
   cd wp-webpack
   ```

2. Install dependencies for the child theme:
   ```bash
   cd wp-content/themes/twentytwentyone-child
   npm install
   ```

## Development

### Build Commands

Navigate to the child theme directory:
```bash
cd wp-content/themes/twentytwentyone-child
```

**Development mode** (watch mode with live reload):
```bash
npm run dev
```

**Production build** (optimized assets):
```bash
npm run prod
```

### Configuration

- **Webpack Config**: Edit `webpack.config.js` to customize build settings
- **Local Domain**: Update the `localDomain` variable in `webpack.config.js` to match your local development URL
- **Entry Points**: Modify the `entryPoints` object to add/remove JavaScript entry files

### BrowserSync

The development build includes BrowserSync for automatic browser reloading. Make sure to update the proxy URL in `webpack.config.js`:

```javascript
const localDomain = 'https://wpwebpack.local'; // Change to your local domain
```

## Build Tools

- **Webpack 4** - Module bundler
- **Babel 7** - JavaScript transpiler
- **Sass** - CSS preprocessor
- **Autoprefixer** - Automatic CSS vendor prefixing
- **BrowserSync** - Live reloading

## Theme Development

The child theme inherits functionality from Twenty Twenty-One and allows you to:

- Customize styles and scripts
- Override parent theme templates
- Add custom functionality via `functions.php`
- Bundle modern JavaScript with ES6+ support

## CI/CD

This project includes GitHub Actions workflow for automated builds. See `.github/workflows/build.yml` for details.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project follows the WordPress Twenty Twenty-One theme license (GPL-2.0-or-later).

## Resources

- [WordPress Theme Development](https://developer.wordpress.org/themes/)
- [Twenty Twenty-One Documentation](https://wordpress.org/themes/twentytwentyone/)
- [Webpack Documentation](https://webpack.js.org/)
- [Babel Documentation](https://babeljs.io/)