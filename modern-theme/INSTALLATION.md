# Modern Theme Installation Guide

## 🎨 What You're Getting

A sophisticated, contemporary redesign of your lab website featuring:

### Design Philosophy
- **Refined Minimalism**: Clean, spacious layouts with intentional accents
- **Scientific Sophistication**: Color palette inspired by neural imaging
- **Modern Typography**: Instrument Serif + Inter for elegant contrast
- **Smooth Interactions**: Thoughtful animations and hover states
- **Professional Polish**: Production-ready design system

### Key Features
- ✨ Custom color system with CSS variables
- 🎯 Refined typography hierarchy
- 💫 Smooth animations and transitions
- 📱 Fully responsive design
- 🎨 Modern card-based layouts
- ⚡ Optimized performance
- ♿ Accessible color contrasts

---

## 📦 Installation

### Quick Install (Recommended)

1. **Download the theme files** from this package:
   - `_styles/custom.scss`
   - `index.md`

2. **Copy to your repository**:
   ```bash
   # Navigate to your local repo
   cd colquittlabsite
   
   # Copy the custom styles
   cp path/to/modern-theme/_styles/custom.scss _styles/custom.scss
   
   # Copy the updated homepage
   cp path/to/modern-theme/index.md index.md
   ```

3. **Commit and push**:
   ```bash
   git add _styles/custom.scss index.md
   git commit -m "Add modern theme"
   git push origin main
   ```

4. **Wait 2-5 minutes** for GitHub Actions to rebuild

5. **Visit** https://colquitt-lab.com to see your new design!

### Alternative: Edit on GitHub

1. **Create the custom.scss file**:
   - Go to: https://github.com/colquittlab/colquittlabsite/tree/main/_styles
   - Click "Add file" → "Create new file"
   - Name it: `custom.scss`
   - Copy content from `_styles/custom.scss` in this package
   - Commit

2. **Update homepage**:
   - Go to: https://github.com/colquittlab/colquittlabsite/blob/main/index.md
   - Click pencil icon to edit
   - Replace with content from `index.md` in this package
   - Commit

---

## 🎨 Design System

### Color Palette

```scss
/* Primary - Deep Scientific Blues */
--primary: #0a2540;
--primary-light: #1e4976;

/* Accents - Vibrant Scientific */
--accent: #00d4ff;          // Cyan (neural activity)
--accent-warm: #ff6b6b;     // Coral (highlights)
--accent-success: #4ecdc4;  // Teal (success states)
--accent-highlight: #ffe66d; // Yellow (important items)
```

### Typography

- **Display**: Instrument Serif (elegant, refined)
- **Body**: Inter (modern, readable)
- **Code**: JetBrains Mono (technical)

### Spacing Scale

Based on 8px grid for visual consistency:
- `--space-1`: 8px
- `--space-2`: 16px
- `--space-3`: 24px
- `--space-4`: 32px
- `--space-5`: 48px
- `--space-6`: 64px
- `--space-7`: 96px
- `--space-8`: 128px

---

## 🛠️ Customization

### Change Colors

Edit `_styles/custom.scss` and modify the color variables:

```scss
:root {
  --primary: #your-color;
  --accent: #your-accent;
  /* etc */
}
```

### Adjust Typography

Change font sizes in the typography section:

```scss
body {
  font-size: 17px; /* Adjust base size */
}

h1 {
  font-size: clamp(2.5rem, 6vw, 4.5rem); /* Responsive sizing */
}
```

### Modify Spacing

Adjust the spacing scale:

```scss
:root {
  --space-4: 2.5rem; /* Was 2rem */
}
```

---

## 🎯 Component Reference

### Cards

```html
<div class="card">
  <h3>Card Title</h3>
  <p>Card content...</p>
</div>
```

Features:
- Hover lift effect
- Accent bar on hover
- Smooth shadows

### Grids

```html
<div class="grid grid-3">
  <div class="card">...</div>
  <div class="card">...</div>
  <div class="card">...</div>
</div>
```

Options:
- `grid-2`: 2-column layout
- `grid-3`: 3-column layout

### Buttons

Using template includes:

```liquid
{% include button.html link="page" text="Click Me" style="primary" %}
{% include button.html link="page" text="Learn More" style="accent" %}
{% include button.html link="page" text="Outline" style="outline" %}
```

### Hero Section

```html
<div class="hero">
  <div class="container">
    <div class="hero-content">
      <span class="hero-tag">Your Tag</span>
      <h1>Your <span class="highlight">Highlighted</span> Title</h1>
      <p class="hero-subtitle">Subtitle text...</p>
    </div>
  </div>
</div>
```

---

## 📱 Responsive Design

The theme is fully responsive with breakpoints at:
- **Desktop**: 1400px max container
- **Tablet**: 768px and below
- **Mobile**: 480px and below

All grids automatically stack on mobile devices.

---

## ⚡ Performance

### Optimization Features
- CSS variables for efficient rendering
- Hardware-accelerated animations
- Optimized font loading
- Minimal JavaScript (CSS-only animations)
- Efficient selectors

### Font Loading

Fonts load from Google Fonts CDN with `display=swap` to prevent render blocking.

---

## 🎭 Animation System

### Fade In Animations

Add to any element:

```html
<div class="animate-fade-in">Content</div>
<div class="animate-fade-in animate-delay-1">Delayed content</div>
```

Delays available: `animate-delay-1`, `animate-delay-2`, `animate-delay-3`

### Hover Effects

Built into components:
- Cards: Lift + accent bar
- Buttons: Lift + shadow
- Team photos: Border color change
- Navigation: Underline animation

---

## 🔧 Troubleshooting

### Styles Not Applying

1. **Check file location**: `_styles/custom.scss` (not `_styles/custom.css`)
2. **Clear browser cache**: Ctrl+Shift+R (or Cmd+Shift+R)
3. **Check GitHub Actions**: Verify build succeeded
4. **Wait**: Sometimes takes 5+ minutes for changes to deploy

### Fonts Not Loading

1. Check internet connection (fonts load from Google CDN)
2. Verify Google Fonts URL is correct in custom.scss
3. Check browser console for errors

### Layout Breaking

1. Ensure you're using the Lab Website Template structure
2. Check for conflicting styles in other scss files
3. Verify container divs are properly closed

### Colors Look Wrong

1. Check CSS variable definitions in `:root`
2. Ensure hex codes are valid (#RRGGBB)
3. Check for browser color profile issues

---

## 🎨 Advanced Customization

### Add New Color

```scss
:root {
  --my-custom-color: #123456;
}

.my-element {
  background: var(--my-custom-color);
}
```

### Create Custom Component

```scss
.my-component {
  padding: var(--space-4);
  background: white;
  border-radius: var(--radius-md);
  box-shadow: var(--shadow-md);
  transition: all var(--transition-base);
}

.my-component:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-lg);
}
```

### Modify Existing Component

Find the component in `custom.scss` and override:

```scss
.card {
  /* Add your customizations */
  border-width: 2px;
  padding: var(--space-5);
}
```

---

## 📚 Resources

### Design Inspiration
- [Instrument Serif Font](https://fonts.google.com/specimen/Instrument+Serif)
- [Inter Font](https://rsms.me/inter/)
- Modern scientific web design trends

### Tools
- [CSS Variables Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [SCSS Documentation](https://sass-lang.com/documentation)
- [Color Contrast Checker](https://webaim.org/resources/contrastchecker/)

---

## 🆘 Getting Help

### Issues with Installation
1. Check this guide first
2. Verify file locations and names
3. Check GitHub Actions for build errors
4. Review browser console for errors

### Design Questions
- The template uses standard SCSS/CSS
- All customizations go in `_styles/custom.scss`
- Use browser DevTools to inspect elements

### Need More Help?
- Template docs: https://greene-lab.gitbook.io/lab-website-template-docs
- SCSS guide: https://sass-lang.com/guide
- CSS reference: https://developer.mozilla.org/en-US/docs/Web/CSS

---

## ✨ What's New

### vs. Default Template

| Feature | Default | Modern Theme |
|---------|---------|--------------|
| Typography | Generic sans-serif | Instrument Serif + Inter |
| Colors | Basic palette | Sophisticated scientific colors |
| Spacing | Inconsistent | 8px grid system |
| Cards | Basic | Elevated with hover effects |
| Animations | Minimal | Smooth, purposeful |
| Layout | Standard | Refined, spacious |
| Overall Feel | Academic | Contemporary + Professional |

---

## 🎉 You're Done!

Your site now has a modern, sophisticated design that:
- ✅ Looks professional and contemporary
- ✅ Maintains accessibility standards
- ✅ Works perfectly on all devices
- ✅ Loads quickly
- ✅ Stands out from typical academic sites

**Enjoy your new design!** 🚀

---

## 📝 Maintenance

### Keeping It Updated

The theme is designed to work with the Lab Website Template. When updating the template:

1. Pull template updates as normal
2. Your custom.scss overrides will be preserved
3. Test after updates to ensure compatibility

### Making Changes

All customizations should go in `_styles/custom.scss` to:
- Keep changes organized
- Avoid conflicts with template updates
- Make it easy to revert if needed

---

**Questions? Check the troubleshooting section or refer to the template documentation!**
