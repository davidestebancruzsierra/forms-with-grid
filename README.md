# Penguin World - Multi-Page Website

## Project Structure

This is a traditional multi-page website built with HTML and CSS. **No JavaScript** is used for navigationall page transitions use standard HTML anchor links.

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
