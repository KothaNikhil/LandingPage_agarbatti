# Divine Agrabatti Landing Page - Enhanced Version

## Project Structure

This enhanced landing page has been reorganized into a modular, scalable structure that makes it easy to manage configuration, styles, and animations.

### File Organization

```
├── index.html              # Main HTML file (refactored to use external files)
├── config.js              # Centralized configuration file (all hardcoded values)
├── colors.css             # Global color variables and utilities
├── typography.css         # Global typography, fonts, and text styles
├── animations.css         # Cool animations and transitions
└── README.md              # This file
```

---

## 📋 Configuration File (`config.js`)

The `config.js` file contains all hardcoded values used throughout the website. This makes it extremely easy to update information without touching HTML.

### What's in config.js:
- **Brand Information**: Name, tagline, founding year, statistics
- **Contact Information**: Address, email, phone number
- **Navigation Links**: All menu links and footer links
- **Products**: Product data with images, names, prices, and categories
- **Media URLs**: Hero image, about image
- **Features**: Feature card information with icons and descriptions
- **Animation Durations**: Timing for animations

### How to Update:
Simply edit the values in `config.js` and they will reflect across the website when integrated with JavaScript.

**Example:**
```javascript
BRAND: {
    name: "Divine Agrabatti",
    tagline: "Essence of Divinity in Every Stick",
    description: "..."
}

CONTACT: {
    address: "123 Temple Road, Mysore, Karnataka 570001",
    email: "hello@divineagrabatti.com",
    phone: "+91 800 123 4567"
}
```

---

## 🎨 Global Styles

### Colors (`colors.css`)

All colors are defined as CSS variables for easy management and consistency.

**Key Color Variables:**
```css
--color-primary: #FAC638
--color-primary-dark: #5216d0
--color-bg-light: #f8f8f5
--color-bg-dark: #231e0f
```

**Usage in HTML:**
- Use Tailwind classes: `bg-primary`, `text-primary-dark`
- Or use CSS variables: `color: var(--color-primary)`

**Benefits:**
- Change all primary colors by editing one variable
- Consistent color scheme across all pages
- Easy to implement dark mode

### Typography (`typography.css`)

Centralized font management with CSS variables for font sizes, weights, and families.

**Key Features:**
- Font family definitions
- Responsive font sizes (scales down on mobile)
- Line height and letter spacing utilities
- Heading styles (h1-h6)
- Material Icons configuration

**Available Font Sizes:**
```css
--text-xs: 0.75rem     (12px)
--text-sm: 0.875rem    (14px)
--text-base: 1rem      (16px)
--text-lg: 1.125rem    (18px)
--text-xl: 1.25rem     (20px)
... up to --text-7xl: 4.5rem (72px)
```

---

## ✨ Animations (`animations.css`)

The landing page now features smooth, professional animations that enhance user experience.

### Available Animation Classes:

#### **Fade Animations**
- `.animate-fade-in` - Fade in element
- `.animate-fade-in-down` - Fade in from top
- `.animate-fade-in-up` - Fade in from bottom
- `.animate-fade-in-left` - Fade in from left
- `.animate-fade-in-right` - Fade in from right

#### **Scale Animations**
- `.animate-scale-in` - Zoom in element
- `.animate-pulse` - Continuous pulse effect
- `.animate-pulse-soft` - Gentle pulsing

#### **Rotate Animations**
- `.animate-rotate` - Continuous rotation
- `.animate-spin` - Spinning effect
- `.animate-rotate-left` - Counter-clockwise rotation

#### **Motion Animations**
- `.animate-bounce` - Bouncy movement
- `.animate-wave` - Wave-like motion
- `.animate-float` - Floating effect
- `.animate-float-slow` - Slower floating

#### **Special Effects**
- `.animate-glow` - Glowing effect
- `.animate-shimmer` - Shimmer animation
- `.animate-blur-in` - Blur-in effect
- `.animate-color-cycle` - Color cycling

#### **Slide Animations**
- `.animate-slide-in-up` - Slide from bottom
- `.animate-slide-in-down` - Slide from top
- `.animate-slide-in-left` - Slide from left
- `.animate-slide-in-right` - Slide from right

#### **Utility Classes**
- `.animate-delay-1` through `.animate-delay-5` - Stagger animations
- `.hover-lift` - Lift on hover
- `.hover-scale-up` - Scale up on hover
- `.transition-smooth` - Smooth transitions

### Animation Timing Variables:
```css
--anim-duration-fast: 300ms
--anim-duration-normal: 500ms
--anim-duration-slow: 700ms
--anim-duration-slower: 1000ms
```

### Example Usage:
```html
<!-- Hero title fades in from top -->
<h1 class="animate-fade-in-down">Essence of Divinity</h1>

<!-- Feature cards fade in with staggered delays -->
<div class="animate-fade-in-up animate-delay-1">Feature 1</div>
<div class="animate-fade-in-up animate-delay-2">Feature 2</div>
<div class="animate-fade-in-up animate-delay-3">Feature 3</div>

<!-- Buttons lift on hover -->
<button class="hover-lift">Shop Now</button>

<!-- Icons with pulse effect -->
<span class="material-symbols-outlined animate-pulse-soft">auto_awesome</span>
```

---

## 🚀 Key Enhancements

### 1. **Cool Animations**
- Hero section: Elements fade and slide in with staggered delays
- Feature cards: Bounce animations with hover lift effects
- Products: Staggered animations with scale-in on hover
- Contact form: Fields animate in sequence
- Icons: Pulsing, spinning, and bouncing effects

### 2. **Centralized Configuration**
- All hardcoded values in `config.js`
- Update once, reflects everywhere
- Perfect for future multi-page sites

### 3. **Global Styles**
- Consistent color scheme across pages
- Reusable typography system
- Easy dark mode support
- Scalable to multiple pages

---

## 📱 Responsive Design

All animations and styles are fully responsive:
- Mobile-first approach
- Adaptive font sizes
- Touch-friendly interactions
- Respects user motion preferences

---

## 🔧 How to Extend

### Adding New Pages:
1. Create a new HTML file
2. Link the same CSS and JS files:
   ```html
   <link href="colors.css" rel="stylesheet"/>
   <link href="typography.css" rel="stylesheet"/>
   <link href="animations.css" rel="stylesheet"/>
   <script src="config.js"></script>
   ```
3. Use the global styles and animations

### Adding New Configuration:
1. Add your data to `config.js` in the CONFIG object
2. Reference it in your HTML/JavaScript

### Adding New Animations:
1. Define the keyframes in `animations.css`
2. Create a utility class
3. Use it in your HTML

### Adding New Colors:
1. Add CSS variables in `colors.css`
2. Create utility classes if needed
3. Use in HTML or CSS

---

## 📝 Best Practices

1. **Always use config.js** for any hardcoded text, links, or data
2. **Use CSS variables** instead of hardcoding colors
3. **Leverage animation classes** for consistent, smooth effects
4. **Keep HTML semantic** and use utility classes for styling
5. **Test animations** on different devices and browsers

---

## 🎯 Animation Performance Tips

- Animations use CSS transforms and opacity (GPU accelerated)
- Respects `prefers-reduced-motion` for accessibility
- Use `.animate-delay-N` classes for staggered animations
- Combine multiple animations for rich effects

---

## 📚 File Sizes

- `config.js`: ~3.5 KB
- `colors.css`: ~3.2 KB
- `typography.css`: ~5.8 KB
- `animations.css`: ~12.5 KB
- `index.html`: Optimized and refactored

**Total additional CSS**: ~21.5 KB (well-optimized)

---

## 🔗 Integration Notes

- All external stylesheets are loaded in the `<head>`
- `config.js` is loaded before body closes (for future JavaScript integration)
- Tailwind CSS is still being used for utility classes
- No conflicting styles between frameworks

---

## ✅ Ready to Scale

This structure is perfect for:
- Adding more pages (products, blog, etc.)
- Creating consistent branding across multiple sites
- Managing large numbers of products
- A/B testing different versions
- Multi-language support (by creating multiple config files)

---

## 🎉 Enjoy Your Enhanced Landing Page!

The landing page now features professional animations, organized structure, and easy-to-manage configuration. Update the config file and extend with confidence!
