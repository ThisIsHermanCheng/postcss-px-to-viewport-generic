# Copilot Instructions for postcss-px-to-viewport-8-plugin-generic

## Project Overview

This repository contains `postcss-px-to-viewport-8-plugin-generic`, a PostCSS plugin that converts `px` units to viewport units (`vw`, `vh`, `vmin`, `vmax`). It's a PostCSS 8 compatible version that resolves deprecation warnings from the original `postcss-px-to-viewport` plugin.

## Key Files and Structure

- **`src/index.ts`** - Main plugin entry point with PostCSS plugin logic
- **`src/types.ts`** - TypeScript type definitions for plugin options
- **`src/utils.ts`** - Utility functions for unit conversion and validation
- **`src/prop-list-matcher.ts`** - Property list matching logic
- **`src/pixel-unit-regexp.ts`** - Regular expressions for pixel unit detection
- **`package.json`** - Package configuration with correct name "postcss-px-to-viewport-8-plugin-generic"
- **`README.md`** - Documentation (should be in English)
- **`spec/`** - Jest test files
- **`example/`** - Usage examples

## Development Guidelines

### Code Style
- Use TypeScript for all source files
- Write all comments in English
- Follow existing code formatting patterns
- Use meaningful variable and function names

### Testing
- Run tests with: `npm test` or `yarn test`
- Tests are located in the `spec/` directory
- Use Jest for testing framework

### Building
- Build with: `npm run build` or `yarn build`
- Uses Father build tool for TypeScript compilation
- Output goes to `lib/` directory

### Key Plugin Concepts
- **Unit Conversion**: Converts `px` to viewport units based on viewport width
- **Property Filtering**: Uses `propList` to specify which CSS properties to convert
- **Selector Exclusion**: Can exclude specific selectors via `selectorBlackList`
- **Ignore Comments**: Supports `/* px-to-viewport-ignore */` to skip conversion
- **Media Query Support**: Optional conversion within media queries

### Configuration Options
The plugin accepts various options including:
- `viewportWidth`: Base viewport width for calculations (default: 320)
- `unitPrecision`: Decimal precision for converted values (default: 5)
- `propList`: Properties to convert (default: ['*'])
- `selectorBlackList`: Selectors to exclude from conversion
- `minPixelValue`: Minimum pixel value to convert (default: 1)
- `mediaQuery`: Whether to convert inside media queries (default: false)

### Common Tasks
- **Adding new features**: Modify `src/index.ts` and update types in `src/types.ts`
- **Bug fixes**: Check utility functions in `src/utils.ts`
- **Documentation updates**: Update `README.md` in English
- **Testing**: Add tests in `spec/` directory following existing patterns

### Important Notes
- All documentation should reference "postcss-px-to-viewport-8-plugin-generic" as the package name
- Maintain compatibility with PostCSS 8+
- Keep comments and documentation in English
- Preserve existing functionality when making changes
- Follow semantic versioning for releases

## PostCSS Plugin Best Practices
- Plugin should return a PostCSS plugin object
- Handle CSS AST nodes properly (Rules, Declarations, AtRules)
- Validate input options and provide meaningful error messages
- Ensure plugin is pure (no side effects)
- Support PostCSS 8 plugin format