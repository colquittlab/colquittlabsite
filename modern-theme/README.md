# Modern Theme for Colquitt Lab Website

## 🎨 Overview

A sophisticated, contemporary redesign for your Jekyll website featuring refined minimalism, modern typography, and smooth interactions.

---

## 📦 What's Included

### 1. **custom.scss** - Complete Design System
   - Modern color palette (deep blues + vibrant accents)
   - Typography system (Instrument Serif + Inter)
   - Component library (cards, buttons, grids)
   - Animation system
   - Responsive layouts
   - 8px spacing grid

### 2. **index.md** - Redesigned Homepage
   - Modern hero section
   - Card-based research focus
   - Feature sections
   - Call-to-action areas
   - Improved content hierarchy

### 3. **INSTALLATION.md** - Complete Guide
   - Step-by-step installation
   - Customization instructions
   - Component reference
   - Troubleshooting
   - Advanced techniques

---

## ⚡ Quick Start

### Installation (5 minutes)

1. **Copy files to your repo**:
   ```bash
   cd colquittlabsite
   cp path/to/modern-theme/_styles/custom.scss _styles/custom.scss
   cp path/to/modern-theme/index.md index.md
   ```

2. **Commit and push**:
   ```bash
   git add _styles/custom.scss index.md
   git commit -m "Add modern theme"
   git push origin main
   ```

3. **Wait 2-5 minutes** → Your new design is live!

### Alternative: Edit on GitHub

1. Create `_styles/custom.scss` with content from this package
2. Update `index.md` with new content
3. Commit changes
4. Done!

---

## ✨ Design Highlights

### Color System
- **Primary**: Deep navy (#0a2540) - Scientific sophistication
- **Accent**: Vibrant cyan (#00d4ff) - Neural activity inspired
- **Warm Accent**: Coral (#ff6b6b) - Highlights and CTAs
- **Neutrals**: Refined gray scale - Professional balance

### Typography
- **Display**: Instrument Serif - Elegant, refined headings
- **Body**: Inter - Modern, highly readable
- **Code**: JetBrains Mono - Technical precision

### Features
- ✨ Smooth hover animations
- 🎯 Card-based layouts with depth
- 💫 Refined spacing (8px grid)
- 📱 Fully responsive
- ⚡ Fast performance
- ♿ Accessible contrasts

---

## 🎯 Key Improvements

### vs. Default Template

| Aspect | Before | After |
|--------|--------|-------|
| **Typography** | Basic sans-serif | Instrument Serif + Inter |
| **Colors** | Generic blues | Scientific palette with vibrant accents |
| **Spacing** | Variable | Consistent 8px grid system |
| **Interactions** | Minimal | Smooth, delightful animations |
| **Cards** | Flat | Elevated with shadows + hover effects |
| **Overall** | Standard academic | Contemporary + sophisticated |

---

## 📁 File Structure

```
modern-theme/
├── _styles/
│   └── custom.scss       # 👈 Main theme file (800+ lines)
├── index.md              # 👈 Redesigned homepage
├── INSTALLATION.md       # Complete setup guide
└── README.md            # This file
```

---

## 🛠️ Installation Methods

### Method 1: Local Copy (Recommended)

**Best for**: Making additional customizations

```bash
# Clone your repo
git clone https://github.com/colquittlab/colquittlabsite.git
cd colquittlabsite

# Copy theme files
cp /path/to/modern-theme/_styles/custom.scss _styles/
cp /path/to/modern-theme/index.md .

# Preview locally
bundle exec jekyll serve

# When satisfied, push
git add _styles/custom.scss index.md
git commit -m "Add modern theme"
git push origin main
```

### Method 2: Direct GitHub Edit

**Best for**: Quick installation

1. Go to https://github.com/colquittlab/colquittlabsite
2. Navigate to `_styles/` folder
3. Create new file: `custom.scss`
4. Paste content from theme's `custom.scss`
5. Commit
6. Edit `index.md` similarly
7. Done!

---

## 🎨 Customization

### Change Primary Color

Edit `_styles/custom.scss`:

```scss
:root {
  --primary: #your-color;
  --primary-light: #your-lighter-color;
}
```

### Adjust Spacing

```scss
:root {
  --space-4: 2.5rem; /* Increase from 2rem */
}
```

### Modify Typography

```scss
body {
  font-size: 18px; /* Increase from 17px */
}
```

### Add Your Own Component

```scss
.my-custom-box {
  padding: var(--space-4);
  background: var(--gray-100);
  border-radius: var(--radius-md);
  box-shadow: var(--shadow-md);
}
```

---

## 📱 Responsive

All layouts automatically adapt to:
- **Desktop**: 1400px max container
- **Tablet**: 768px breakpoint
- **Mobile**: Single column layouts

Grids stack automatically on smaller screens.

---

## 🎭 Animation System

### Built-in Animations

```html
<!-- Fade in on page load -->
<div class="animate-fade-in">Content</div>

<!-- With delay -->
<div class="animate-fade-in animate-delay-1">Delayed content</div>
<div class="animate-fade-in animate-delay-2">More delay</div>
```

### Hover Effects

Automatic on:
- Cards (lift + accent bar)
- Buttons (lift + shadow)
- Team member photos (border color)
- Citations (left border + translate)
- Navigation links (underline)

---

## 🔧 Troubleshooting

### Styles Not Showing

1. ✅ Clear browser cache (Ctrl+Shift+R)
2. ✅ Wait 5 minutes for deployment
3. ✅ Check GitHub Actions succeeded
4. ✅ Verify file is at `_styles/custom.scss`

### Fonts Not Loading

1. ✅ Check internet connection
2. ✅ Verify Google Fonts URL in custom.scss
3. ✅ Check browser console for errors

### Build Failing

1. ✅ Check SCSS syntax (especially brackets and semicolons)
2. ✅ View GitHub Actions error messages
3. ✅ Ensure no duplicate `:root` blocks

---

## 📚 Component Library

### Cards

```html
<div class="card">
  <h3>Title</h3>
  <p>Content</p>
</div>
```

### Grids

```html
<div class="grid grid-3">
  <div class="card">...</div>
  <div class="card">...</div>
  <div class="card">...</div>
</div>
```

### Hero Section

```html
<div class="hero">
  <div class="container">
    <div class="hero-content">
      <span class="hero-tag">Tag</span>
      <h1>Title with <span class="highlight">Highlight</span></h1>
      <p class="hero-subtitle">Subtitle</p>
    </div>
  </div>
</div>
```

### Buttons (via template)

```liquid
{% include button.html link="page" text="Primary" style="primary" %}
{% include button.html link="page" text="Accent" style="accent" %}
{% include button.html link="page" text="Outline" style="outline" %}
```

---

## 💡 Pro Tips

1. **Preview locally first** before pushing major changes
2. **Use CSS variables** for all customizations to maintain consistency
3. **Keep custom.scss organized** by component for easy maintenance
4. **Test on mobile** after significant layout changes
5. **Check accessibility** - all colors meet WCAG AA standards

---

## 🎯 Next Steps

### After Installation

1. ✅ Verify site looks correct on desktop and mobile
2. ✅ Update other pages (research, team, contact) with similar style
3. ✅ Add your lab photos to match new design
4. ✅ Consider customizing colors to match lab branding

### Optional Enhancements

- Add custom hero images
- Create additional custom components
- Adjust colors to your preference
- Add more animations
- Create page-specific styles

---

## 📖 Documentation

- **INSTALLATION.md** - Detailed setup and customization guide
- **Template Docs** - https://greene-lab.gitbook.io/lab-website-template-docs
- **SCSS Guide** - https://sass-lang.com/guide
- **CSS Variables** - https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties

---

## 🆘 Support

### Need Help?

1. Check **INSTALLATION.md** for detailed guidance
2. Review browser console for errors
3. Check GitHub Actions for build issues
4. Consult template documentation

### Common Questions

**Q: Can I revert to the old design?**  
A: Yes! Just delete `_styles/custom.scss` and restore `index.md`

**Q: Will this break my existing content?**  
A: No! The theme only adds styles, doesn't remove functionality

**Q: Can I mix old and new styles?**  
A: Yes, custom.scss works alongside template defaults

---

## ✨ Features at a Glance

### Visual Design
- ✅ Modern color system with CSS variables
- ✅ Refined typography (Instrument Serif + Inter)
- ✅ Consistent 8px spacing grid
- ✅ Sophisticated shadow system
- ✅ Smooth transitions and animations

### Components
- ✅ Elevated cards with hover effects
- ✅ Modern button styles
- ✅ Flexible grid layouts
- ✅ Hero sections
- ✅ Team member cards
- ✅ Citation styles

### Technical
- ✅ Fully responsive
- ✅ Performance optimized
- ✅ Accessible color contrasts
- ✅ Cross-browser compatible
- ✅ Mobile-first approach

---

## 🎉 Ready to Install!

Your new modern theme is ready to transform your lab website into a contemporary, professional showcase.

**Start with the Quick Start section above**, or dive into **INSTALLATION.md** for detailed instructions.

---

**Questions? Check INSTALLATION.md for comprehensive guidance!**
