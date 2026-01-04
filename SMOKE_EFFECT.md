# 🌫️ Smoke Effect Documentation

## NEW FEATURE: Light Smoke Animation

A beautiful light smoke effect has been added to the hero section background for enhanced visual appeal.

---

## 🎬 What Was Added

### Smoke Animations (animations.css)
Three unique smoke movement patterns:

1. **smokeDrift** - Horizontal drift upward
2. **smokeFloat** - Gentle floating motion
3. **smokeSwirl** - Swirling circular motion

### Smoke Particles (index.html)
6 smoke particles positioned around the hero section:
- Different sizes (100px - 150px)
- Varying animation speeds (8s - 12s)
- Staggered animation delays (0s - 5s)
- Smooth opacity transitions

---

## 🎨 Visual Details

**Smoke Styling:**
- Radial gradient white to gray
- Heavy blur effect (20px)
- Semi-transparent (0.4 - 0.6 opacity)
- Circular shape with rounded borders

**Animation Properties:**
- GPU-accelerated transforms
- Smooth easing functions
- Continuous infinite loop
- Non-intrusive (pointer-events: none)

---

## 📍 Where It Appears

**Location**: Hero section background
**Coverage**: Full width and height
**Layers**: Behind text, images, and main content
**Effect**: Floating ethereal smoke clouds

---

## 🔧 How to Customize

### Adjust Smoke Opacity
Open `animations.css`, find `.smoke-particle`:
```css
.smoke-particle {
    background: radial-gradient(circle at 30% 30%, rgba(255, 255, 255, 0.8), rgba(200, 200, 200, 0.1));
    /* Change 0.8 and 0.1 for more/less opacity */
}
```

### Change Smoke Color
Modify the rgba values in the gradient:
```css
/* From white/gray to custom color */
rgba(255, 255, 255, 0.8) → rgba(250, 198, 56, 0.6)
```

### Adjust Animation Speed
Modify the animation durations in smoke particle classes:
```css
.smoke-particle-1 {
    animation: smokeDrift 8s ease-in-out infinite;
    /* Change 8s to 6s (faster) or 12s (slower) */
}
```

### Add More Particles
Add new smoke-particle divs in index.html:
```html
<div class="smoke-particle smoke-particle-7" style="left: 25%; top: 45%;"></div>
```
Add corresponding CSS in animations.css:
```css
.smoke-particle-7 {
    width: 125px;
    height: 125px;
    animation: smokeFloat 13s ease-in-out infinite;
    animation-delay: 6s;
}
```

### Remove Smoke Effect
Simply delete the smoke particles div block from index.html:
```html
<!-- Delete this entire section -->
<div class="absolute inset-0 overflow-hidden pointer-events-none">
    <!-- All smoke particles -->
</div>
```

---

## 🎯 Animation Details

### smokeDrift (8-11 seconds)
- Moves right and upward
- Gradually fades in and out
- Creates horizontal flow

**Used by:** smoke-particle-1, smoke-particle-4

### smokeFloat (10-12 seconds)
- Gentle upward movement
- Slight scaling effect
- Soft appearance

**Used by:** smoke-particle-2, smoke-particle-5

### smokeSwirl (9-10 seconds)
- Moves diagonally
- Rotates 180 degrees
- Creates swirling effect

**Used by:** smoke-particle-3, smoke-particle-6

---

## 💡 Pro Tips

1. **Combine with colors**: Use smoke with different blend modes
2. **Increase particles**: Add more for denser effect
3. **Adjust blur**: Higher blur = softer, lighter effect
4. **Vary speeds**: Different durations create natural randomness
5. **Use in other sections**: Copy smoke code to about or contact sections

---

## 🎨 Configuration (config.js)

New configuration added:
```javascript
SMOKE_EFFECT: {
    enabled: true,
    opacity: 0.4,
    blur: "20px",
    particles: 6,
    animationType: ["smokeDrift", "smokeFloat", "smokeSwirl"]
}
```

**Customize smoke settings** here for easy global control (future JavaScript integration).

---

## ✨ Visual Impact

**Before**: Clean gradient background with glows
**After**: Ethereal, mystical atmosphere with floating smoke

Perfect for:
- Wellness/spa products ✓
- Incense/fragrance brands ✓
- Spiritual/meditation themes ✓
- Premium luxury positioning ✓

---

## 📱 Browser Support

- ✅ Chrome/Edge (full support)
- ✅ Firefox (full support)
- ✅ Safari (full support)
- ✅ Mobile browsers (optimized)

---

## 🚀 What's Next

You can:
1. Add smoke to other sections (about, contact)
2. Change smoke colors to brand colors
3. Adjust animation speeds for different effects
4. Increase particles for denser smoke
5. Combine with other effects for enhanced visuals

---

**Status**: ✅ Active
**Performance**: High (GPU-accelerated)
**Accessibility**: ✅ Respects motion preferences
