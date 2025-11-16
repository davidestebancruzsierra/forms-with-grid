# Penguin World - Multi-Page Website

## Authors

**David Esteban Cruz Sierra** - Developer & Designer

## Project Overview

This is a traditional multi-page website built with HTML and CSS. **No JavaScript** is used for navigation—all page transitions use standard HTML anchor links.

### Pages

- **index.html** - Home page with welcome message and penguin facts
- **about.html** - About us page
- **services.html** - Services with in-page fragment navigation (#tours, #conservation, etc.)
- **contact.html** - Contact information
- **antarctica.html** - Antarctica penguin habitat
- **southamerica.html** - South America penguin habitat
- **africa.html** - Africa penguin habitat
- **oceania.html** - Oceania penguin habitat
- **australia.html** - Australia penguin habitat

### Technologies

- **HTML5** - Semantic markup with proper anchor navigation
- **CSS3** - External stylesheet (styles.css) with Flexbox layouts
- **No JavaScript** - Pure HTML navigation using href attributes

### Navigation

- **Inter-page navigation**: Standard `<a href="page.html">` links
- **Fragment navigation**: In-page anchors using `<a href="#section">` (see services.html)
- **SEO-friendly**: All links are crawlable by search engines
- **Accessible**: Proper semantic HTML structure

### CSS Features

- Flexbox-based layouts throughout
- Responsive design with media queries
- Smooth scroll behavior via CSS
- No floats (replaced with flexbox media components)

### How to View

Simply open `index.html` in a web browser. All navigation works without a web server.

### Original SPA Version

The original Single Page Application version has been backed up to `index-spa-backup.html` for reference.

---

## Biggest Challenges & Solutions

### Challenge 1: File Organization & Route Management
**Problem:** After reorganizing all HTML files into logical folders (`Pages/Contact Us/` and `Pages/Continents/`), all internal links and resource paths broke.

**Solution:** Systematically updated all routes across 18+ HTML files:
- Root files use `Pages/Contact Us/` and `Pages/Continents/`
- Files in subfolders use `../../` for root resources (CSS, assets)
- Files in subfolders use `../` for sibling folders
- Used multi-replace operations for efficiency (fixed 17 image paths in one operation)

### Challenge 2: CSS Modularization
**Problem:** Original `styles.css` was 1,695 lines and difficult to maintain.

**Solution:** Split into 13 modular CSS files organized by component/page:
- Base styles, header, layout, images, sidebar, footer
- Page-specific styles (Australia, 4 contact form variations)
- Responsive styles separate for clarity
- Created `styles-new.css` with @import statements to maintain compatibility

### Challenge 3: Phone Number Input with Dropdown
**Problem:** Needed a country code selector with dropdown arrow that integrated seamlessly with the phone number field.

**Solution:** Used CSS pseudo-elements and background SVG:
```css
.country-code {
    width: 80px;
    appearance: none;
    background-image: url("data:image/svg+xml,...");
    background-repeat: no-repeat;
    background-position: right 8px center;
}
```

### Challenge 4: Responsive Grid Layouts
**Problem:** Form layouts needed to work on mobile, tablet, and desktop without breaking.

**Solution:** CSS Grid with responsive media queries:
```css
.form-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 30px;
}

@media (max-width: 768px) {
    .form-grid {
        grid-template-columns: 1fr;
    }
}
```

---

## Course Requirements Completed

This project fulfills all 30 requirements for Course 1:
- ✅ HTML5 boilerplate, semantic structure, proper formatting
- ✅ Multi-page navigation with fragment links
- ✅ Inline, internal, and external CSS
- ✅ Block, inline, and inline-block display examples
- ✅ Type, class, and ID selectors
- ✅ Complete box model implementation
- ✅ All link pseudo-classes (:link, :visited, :hover, :active)
- ✅ Float and clear properties
- ✅ Flexbox and Grid layouts
- ✅ Overflow property examples
- ✅ Comprehensive CSS comments and organization

See `PROJECT_CHECKLIST.md` for detailed requirement mapping.
