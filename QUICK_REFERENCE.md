# Quick Reference Guide

## 📋 Quick Links

| File | Purpose | When to Edit |
|------|---------|--------------|
| `config.js` | All text, links, products | Updating content |
| `colors.css` | Color scheme | Changing brand colors |
| `typography.css` | Fonts & sizes | Font family changes |
| `animations.css` | Animation effects | New animations needed |
| `index.html` | HTML structure | Adding new sections |

---

## 🎬 Animation Cheat Sheet

### Common Animations
```html
<!-- Fade in from top -->
<div class="animate-fade-in-down">Content</div>

<!-- Fade in from bottom with delay -->
<div class="animate-fade-in-up animate-delay-2">Content</div>

<!-- Scale in -->
<div class="animate-scale-in">Content</div>

<!-- Bounce icon -->
<span class="material-symbols-outlined animate-bounce">emoji</span>

<!-- Pulse effect -->
<div class="animate-pulse-soft">Content</div>

<!-- Rotate/Spin -->
<span class="material-symbols-outlined animate-spin">spinner</span>

<!-- Lift on hover -->
<button class="hover-lift">Click Me</button>

<!-- Floating effect -->
<div class="animate-float">Content</div>
```

### Delay Levels
```html
animate-delay-1   (0.1s)
animate-delay-2   (0.2s)
animate-delay-3   (0.3s)
animate-delay-4   (0.4s)
animate-delay-5   (0.5s)
```

---

## 🎨 Color Reference

### Primary Colors
```css
--color-primary: #FAC638 (Gold/Yellow)
--color-primary-dark: #5216d0 (Purple)
```

### Background
```css
--color-bg-light: #f8f8f5 (Light)
--color-bg-dark: #231e0f (Dark)
```

### Accent Colors
```css
Green:   #16a34a
Orange:  #ea580c
Purple:  #a855f7
Yellow:  #ca8a04
```

### How to Use
```html
<!-- In HTML (with Tailwind) -->
<div class="text-primary">Gold text</div>
<div class="bg-primary-dark">Purple background</div>

<!-- In CSS -->
color: var(--color-primary);
background: var(--color-bg-dark);
```

---

## 📝 Config.js Quick Edit

### Change Brand Name
```javascript
BRAND: {
    name: "Your New Name",  // ← Change this
    tagline: "Your tagline",
    // ...
}
```

### Add/Remove Products
```javascript
PRODUCTS: [
    {
        id: 1,
        name: "Product Name",
        category: "Category",
        price: 15.00,
        image: "image-url"
    },
    // Add more or remove existing
]
```

### Update Contact Info
```javascript
CONTACT: {
    address: "Your address",      // ← Change
    email: "your@email.com",      // ← Change
    phone: "+91 800 123 4567"     // ← Change
}
```

---

## 🚀 Common Tasks

### Task: Change Hero Title
1. Open `config.js`
2. Find `BRAND.tagline`
3. Update text
4. Save
✅ Changes everywhere automatically!

### Task: Change Primary Color
1. Open `colors.css`
2. Find `--color-primary: #FAC638`
3. Change to new color (e.g., `#FF5733`)
4. Save
✅ All gold colors update instantly!

### Task: Add New Feature
1. Open `config.js`
2. Find `FEATURES` array
3. Add new feature object:
```javascript
{
    icon: "star",
    title: "New Feature",
    description: "Feature description",
    bgColor: "bg-blue-100",
    // ... other properties
}
```

### Task: Slow Down Animations
1. Open `animations.css`
2. Find `--anim-duration-normal: 500ms`
3. Change to `700ms` or higher
4. Save
✅ All animations now slower!

### Task: Add Hover Effect to Button
```html
<button class="hover-lift">My Button</button>
```
Or with scale:
```html
<button class="hover:scale-105 transition-transform">My Button</button>
```

---

## 📱 Testing Checklist

- [ ] Desktop view (1920px)
- [ ] Tablet view (768px)
- [ ] Mobile view (375px)
- [ ] Dark mode
- [ ] Light mode
- [ ] Animations smooth
- [ ] No layout shifts
- [ ] Links working
- [ ] Contact form responsive

---

## 🔧 Useful CSS Variables

```css
/* Animations */
--anim-duration-fast: 300ms
--anim-duration-normal: 500ms
--anim-duration-slow: 700ms

/* Fonts */
--font-display: 'Manrope'
--text-lg: 1.125rem
--text-3xl: 1.875rem

/* Colors */
--color-primary: #FAC638
--color-gray-900: #111827
```

---

## 🎯 Structure Map

```
┌─ index.html ─────────────── Main page
│  └─ Links to CSS & JS
│
├─ config.js ──────────────── All data/content
│
├─ colors.css ─────────────── Color scheme
│  └─ 40+ color variables
│
├─ typography.css ────────── Fonts & text
│  └─ Font sizes, weights
│
├─ animations.css ────────── Animation effects
│  └─ 20+ animations
│
└─ Documentation
   ├─ README.md
   └─ This file
```

---

## 💡 Pro Tips

1. **Batch Updates**: Update multiple config values at once in `config.js`
2. **Color Palettes**: Create multiple config files for different themes
3. **Animation Testing**: Use browser DevTools to slow down animations for testing
4. **Mobile First**: Test on mobile before desktop
5. **Accessibility**: Already includes motion preference support

---

## ❓ FAQ

**Q: Where are all the product names?**
A: In `config.js` under `PRODUCTS` array

**Q: How do I change the gold color?**
A: Edit `--color-primary` in `colors.css`

**Q: Can I reuse these files on other pages?**
A: Yes! Link the same CSS files and use `config.js` for shared data

**Q: How do I add more animations?**
A: Create keyframes in `animations.css` and add utility classes

**Q: Will animations work on mobile?**
A: Yes! They're optimized and respects motion preferences

**Q: Can I change animation speed?**
A: Yes! Edit `--anim-duration-*` variables in `animations.css`

---

## 📞 Quick Support

| Issue | Solution |
|-------|----------|
| Text not updating | Check `config.js` |
| Colors wrong | Check `colors.css` variables |
| Animations missing | Check `animations.css` |
| Styles broken | Verify all CSS files linked |
| Layout shift | Check CSS specificity |

---

**Last Updated**: January 2026
**Version**: 1.0 Enhanced
**Status**: ✅ Production Ready
