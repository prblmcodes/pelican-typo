# pelican-typo

A typography-focused theme for [Pelican](https://getpelican.com/) with automatic dark/light mode and 9 color schemes.

## Features

- **9 Color Schemes** - Default, Gruvebox, Catpuccin, E-ink, Base16 (Default, Ocean, Eighties, Cupcake, Mocha)
- **Typography First** - Literata serif font for body text, Monaspace monospace for code
- **Dark/Light Mode** - Automatic detection of system preference with manual toggle support
- **KaTeX Math Support** - Optional LaTeX math rendering
- **Mermaid Diagrams** - Built-in support for Mermaid diagram rendering
- **Code Copy Button** - One-click code block copying
- **Responsive Design** - Mobile-friendly layout with breakpoints at 1024px, 768px, and 640px
- **RSS/Atom Feeds** - Full feed support including category and tag feeds

## Installation

### Clone repository in your project using

```bash
git clone https://github.com/prblmcodes/pelican-typo.git
```

Then set in your `pelicanconf.py`:

```python
THEME = '/path/to/pelican-themes/pelican-typo'
```

Or downlod the `pelican-typo` as zip file and copy the `pelican-typo` folder directly into your project's themes directory.

## Configuration

Add to your `pelicanconf.py`:

```python
# Required
THEME = 'path/to/pelican-typo'

# Required
PATH = "content"

# Theme color scheme (optional, defaults to 'default')
THEME_COLOR = 'default'  # See color schemes below

# Pass color theme to templates
JINJA_GLOBALS = {
    'color_theme': THEME_COLOR
}

# Theme mode: 'auto', 'light', or 'dark' (optional)
THEME_SETTING = {
    'theme': 'auto',
}

# Enable KaTeX math support (optional)
USE_MATH = True

# Display settings (optional)
DISPLAY_PAGES_ON_MENU = True
DISPLAY_CATEGORIES_ON_MENU = True

# Menu items (optional)
MENUITEMS = (
    ('Archives', '/archives.html'),
    ('Tags', '/tags.html'),
)
```

## Color Schemes

| Scheme | Description |
|--------|-------------|
| `default` | Clean black and white with subtle grays |
| `gruvebox` | Warm, retro groove colors |
| `catpuccin` | Soothing pastel theme |
| `eink` | High contrast e-reader style |
| `base16-default` | Base16 default dark/light |
| `base16-ocean` | Base16 ocean colors |
| `base16-eighties` | Base16 eighties palette |
| `base16-cupcake` | Base16 cupcake pastels |
| `base16-mocha` | Base16 mocha tones |

To use a color scheme, set `THEME_COLOR` in your config:

```python
THEME_COLOR = 'gruvebox'
```

## Templates

The theme includes the following templates:

| Template | Purpose |
|----------|---------|
| `index.html` | Homepage with article list and pagination |
| `article.html` | Individual article page |
| `page.html` | Static page |
| `archives.html` | All articles by date |
| `period_archives.html` | Articles for a specific period |
| `categories.html` | List of all categories |
| `category.html` | Articles in a specific category |
| `tags.html` | List of all tags |
| `tag.html` | Articles with a specific tag |
| `authors.html` | List of all authors |
| `author.html` | Articles by a specific author |
| `pagination.html` | Pagination partial |
| `translations.html` | Translation links |
| `layout/base.html` | Base template |
| `partials/header.html` | Site header and navigation |
| `partials/footer.html` | Site footer |
| `partials/sub_head.html` | Meta tags and CSS includes |
| `partials/math.html` | KaTeX math support |

## Customization

### Custom CSS

Add custom styles by editing `static/css/custom.css`.

### Custom Color Scheme

Create a new CSS file in `static/css/colors/` following this structure:

```css
:root {
    --content-primary: rgb(36, 36, 36);
    --content-secondary: rgb(117, 117, 117);
    --background: rgb(255, 255, 255);
    --code-background: rgb(249, 249, 249);
    --code-border: rgb(229, 229, 229);
}

.dark {
    --content-primary: rgb(218, 218, 218);
    --content-secondary: rgb(140, 140, 140);
    --background: rgb(20, 20, 20);
    --code-background: rgb(30, 30, 30);
    --code-border: rgb(50, 50, 50);
}
```

Then reference your scheme name in `THEME_COLOR`.

## Font Licensing

This theme includes the following fonts under the SIL Open Font License:

- **[Literata](https://github.com/googlefonts/literata)** - Variable serif typeface by TypeTogether
- **[Monaspace](https://github.com/githubnext/monaspace)** - Monospace type system by GitHub Next

Both fonts are licensed under the [SIL Open Font License 1.1](https://scripts.sil.org/OFL).

## Credits

Developed by **prblm**

## License

MIT License - see [LICENSE](LICENSE) file for details.
