# MullenCreates Design System

A comprehensive, modular design system built with BEM methodology, optimized for WordPress Gutenberg blocks and reusable across projects.

## 📁 Files Structure

```
/
├── design-system-complete.html      # Complete design system page
├── design-system-variables.scss     # SCSS variables and design tokens
├── component-color-palette.html     # Standalone color palette component
├── component-typography.html        # Standalone typography component  
├── component-buttons.html           # Standalone buttons component
├── component-cards-forms.html       # Standalone cards & forms component
└── README.md                        # This documentation
```

## 🎨 Design System Overview

### Design Tokens
The system is built on a foundation of design tokens (CSS custom properties) that ensure consistency across all components:

- **Colors**: Primary, secondary, neutral, and semantic colors
- **Typography**: Font families, sizes, weights, and line heights
- **Spacing**: Consistent spacing scale from 4px to 128px
- **Border Radius**: From 2px to 16px rounded corners
- **Shadows**: Five levels of elevation
- **Breakpoints**: Mobile-first responsive design points

### BEM Methodology
All components follow BEM (Block Element Modifier) naming convention:
- **Block**: `.styleguide__[component-name]`
- **Element**: `.styleguide__[component-name]__[element]`
- **Modifier**: `.styleguide__[component-name]--[modifier]`

## 🧩 Components

### 1. Color Palette Component
**File**: `component-color-palette.html`
**Block**: `.styleguide__color-palette`

Displays brand colors with hex codes and usage guidelines.

**Usage**:
```html
<div class="styleguide__color-palette">
    <!-- Color swatches automatically display -->
</div>
```

**Key Classes**:
- `.styleguide__color-swatch` - Individual color card
- `.styleguide__color-swatch__sample--[color]` - Color sample variations
- `.styleguide__color-swatch__info` - Color information container

### 2. Typography Component
**File**: `component-typography.html`
**Block**: `.styleguide__typography`

Showcases heading styles, body text, and typography hierarchy.

**Usage**:
```html
<div class="styleguide__typography">
    <!-- Typography samples automatically display -->
</div>
```

**Key Classes**:
- `.styleguide__type-sample` - Container for each type specimen
- `.styleguide__type-sample__element--[type]` - Specific element styling
- `.styleguide__type-sample__link` - Link styling within text

### 3. Buttons Component
**File**: `component-buttons.html`
**Block**: `.styleguide__buttons`

Complete button system with multiple variants and sizes.

**Usage**:
```html
<!-- Primary Button -->
<a href="#" class="styleguide__btn styleguide__btn--primary">Primary Action</a>

<!-- Outline Button -->
<a href="#" class="styleguide__btn styleguide__btn--outline">Secondary Action</a>

<!-- Small Button -->
<a href="#" class="styleguide__btn styleguide__btn--primary styleguide__btn--small">Small</a>

<!-- Large Button -->
<a href="#" class="styleguide__btn styleguide__btn--primary styleguide__btn--large">Large</a>

<!-- Disabled Button -->
<button class="styleguide__btn styleguide__btn--primary" disabled>Disabled</button>
```

**Button Variants**:
- `--primary` - Main call-to-action buttons
- `--outline` - Secondary action buttons
- `--secondary` - Tertiary/neutral buttons

**Button Sizes**:
- `--small` - Compact buttons
- `--large` - Prominent buttons
- (default) - Standard size

### 4. Cards & Forms Component
**File**: `component-cards-forms.html`
**Block**: `.styleguide__cards-forms`

Comprehensive card layouts and form elements with validation states.

**Card Usage**:
```html
<div class="styleguide__card">
    <h3 class="styleguide__card__title">Card Title</h3>
    <p class="styleguide__card__content">Card content goes here.</p>
    <div class="styleguide__card__actions">
        <a href="#" class="styleguide__btn styleguide__btn--primary">Action</a>
    </div>
</div>
```

**Form Usage**:
```html
<form class="styleguide__form">
    <div class="styleguide__form-group">
        <label class="styleguide__form__label" for="input-id">Label</label>
        <input type="text" id="input-id" class="styleguide__form__input" placeholder="Placeholder">
    </div>
</form>
```

**Card Variants**:
- `--highlight` - Emphasized card with border
- `--image` - Card with image header

**Form States**:
- `--valid` - Success/valid state
- `--error` - Error state
- `:disabled` - Disabled state

## 🎯 WordPress Gutenberg Integration

All components are optimized for WordPress Gutenberg blocks:

1. **Container Compatibility**: Works within `.wp-block-group` containers
2. **Responsive Design**: Mobile-first approach matches WordPress standards
3. **Accessibility**: ARIA support and keyboard navigation
4. **CSS Variables**: Easy customization through WordPress customizer

**Example Gutenberg Integration**:
```html
<div class="wp-block-group">
    <div class="styleguide__color-palette">
        <!-- Color palette component -->
    </div>
</div>
```

## 📱 Responsive Design

The design system follows a mobile-first approach with these breakpoints:

- **Mobile**: 0-767px
- **Tablet**: 768-1023px  
- **Desktop**: 1024px+

**Key responsive features**:
- Fluid typography using `clamp()`
- Flexible grid layouts with `minmax()`
- Touch-friendly interaction targets (44px minimum)
- Optimized spacing for mobile devices

## ♿ Accessibility Features

- **Color Contrast**: WCAG AA compliant color ratios
- **Keyboard Navigation**: Full keyboard accessibility
- **Focus Management**: Visible focus indicators
- **Screen Reader Support**: Semantic HTML structure
- **Reduced Motion**: Respects `prefers-reduced-motion`
- **High Contrast**: Adapts to `prefers-contrast: high`

## 🎨 Customization

### CSS Custom Properties
Customize the design system by overriding CSS variables:

```css
:root {
    --color-primary: #your-brand-color;
    --font-family-heading: 'Your Font', serif;
    --border-radius-base: 8px;
}
```

### SCSS Variables
Use the provided SCSS variables file for more advanced customization:

```scss
@import 'design-system-variables';

// Override variables
$color-primary: #your-brand-color;
$font-family-primary: 'Your Font', sans-serif;
```

## 🚀 Usage Instructions

### Option 1: Complete System
Use the complete design system page:
```html
<!-- Copy the entire content from design-system-complete.html -->
```

### Option 2: Individual Components
Include only the components you need:
```html
<!-- Include individual component files -->
<link rel="stylesheet" href="component-buttons.html">
```

### Option 3: Custom Implementation
1. Include the SCSS variables file
2. Copy the CSS for specific components
3. Customize colors and spacing as needed

## 📝 Best Practices

### Component Usage
1. **Consistency**: Use the same component variants across your project
2. **Hierarchy**: Only one primary button per section
3. **Accessibility**: Always include proper labels and ARIA attributes
4. **Responsive**: Test components on all device sizes

### Code Organization
1. **BEM Structure**: Follow the established naming convention
2. **CSS Variables**: Use custom properties for theming
3. **Semantic HTML**: Use appropriate HTML elements
4. **Performance**: Minimize CSS by only including needed components

### WordPress Integration
1. **Block Patterns**: Create reusable block patterns with these components
2. **Theme Integration**: Add components to your theme's stylesheet
3. **Customizer**: Make key variables customizable through WordPress customizer
4. **Plugin Compatibility**: Test with common WordPress plugins

## 🔧 Development Workflow

### Setting Up
1. Copy the desired component files to your project
2. Include the CSS in your build process
3. Test responsive behavior
4. Validate accessibility compliance

### Customizing Colors
1. Update the color variables in `:root`
2. Test color contrast ratios
3. Verify consistency across all components
4. Update documentation with new color values

### Adding New Components
1. Follow the established BEM naming convention
2. Use existing design tokens (spacing, colors, typography)
3. Include responsive styles
4. Add accessibility features
5. Test in WordPress Gutenberg environment

## 📞 Support

For questions or issues with the MullenCreates Design System:

1. **Documentation**: Refer to this README and component comments
2. **Testing**: Validate components in your target environment
3. **Customization**: Use CSS custom properties for theming
4. **Accessibility**: Test with screen readers and keyboard navigation

## 📄 License

This design system is created for MullenCreates and follows their brand guidelines. Components can be adapted for other projects while maintaining accessibility and responsive design principles.

---

**Version**: 1.0  
**Last Updated**: January 2025  
**Compatibility**: WordPress 6.0+, Modern Browsers
