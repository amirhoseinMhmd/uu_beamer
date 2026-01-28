# Utrecht University Beamer Theme

A LaTeX Beamer presentation theme for Utrecht University, based on the official brand guidelines.

## Compilation

This theme supports multiple LaTeX compilers:

- **pdfLaTeX** - Works out of the box with fallback fonts (Latin Modern)
- **XeLaTeX** - Recommended for full font support (Merriweather, Open Sans)
- **LuaLaTeX** - Also supports full font features

```bash
# Using pdfLaTeX (simplest, works everywhere)
pdflatex example.tex

# Using XeLaTeX (recommended for best typography)
xelatex example.tex

# Using LuaLaTeX
lualatex example.tex
```

## Color Palette

### Primary Colors (Official UU Brand)
- **Yellow** (#FFCD00) - The distinctive Utrecht University color
- **Red** (#C00A35) - Accent color
- **Black** (#000000)
- **White** (#FFFFFF)

### Secondary Colors (for data visualizations, infographics)
- **Cream** (#FFE6AB)
- **Orange** (#F3965E)
- **Burgundy** (#AA1555)
- **Brown** (#6E3B23)
- **Green** (#24A793)
- **Blue** (#5287C6)
- **Dark Blue** (#001240)
- **Purple** (#7D4E8D)

## Installation

1. Copy all `.sty` files to your LaTeX project directory or install them in your TeX distribution.
2. Copy the `graphics` folder with `corner-logo.png` and `circles.png`.
3. Optionally copy the `styles` folder for matplotlib integration.

## Usage

```latex
\documentclass[aspectratio=169, 10pt]{beamer}
\usetheme{uu}

% Optional: Set footer text
\setuufootleft{Your Name --- Utrecht University}

\title{Your Presentation Title}
\author{Your Name}
\institute{Faculty or Department}

\begin{document}
    \begin{frame}[plain]
        \titlepage
    \end{frame}
    
    % Your content here
    
    \begin{frame}[plain]
        \Closure{Thank you}{Questions?}
    \end{frame}
\end{document}
```

## Theme Options

### Style Variants
While Utrecht University has moved away from faculty-specific colors, this theme provides optional style variants using the secondary color palette:

```latex
\usetheme[style=science]{uu}    % Blue
\usetheme[style=law]{uu}        % Burgundy
\usetheme[style=medicine]{uu}   % Green
\usetheme[style=humanities]{uu} % Dark Blue
\usetheme[style=social]{uu}     % Orange
\usetheme[style=geosciences]{uu}% Brown
\usetheme[style=veterinary]{uu} % Purple
```

### Other Options
- `noslidenumbering` - Disable slide numbers

```latex
\usetheme[noslidenumbering]{uu}
```

## Special Features

### Accent Colors
Use `\accent[color]{text}` to highlight text with theme colors:

```latex
\accent{default red highlight}
\accent[yellow]{yellow highlight}
\accent[green]{green highlight}
\accent[blue]{blue highlight}
```

### Standout Frames
Create emphasis slides with reversed colors:

```latex
\begin{frame}[standout]
    Important message here
\end{frame}
```

### Closing Slide
Use the `\Closure` command for a styled closing slide:

```latex
\begin{frame}[plain]
    \Closure{Thank you}{Questions?}
\end{frame}
```

## Fonts

The theme uses:
- **Merriweather** - Main text font (official UU font)
- **Open Sans** - Alternative sans-serif font (official UU font)
- **IBM Plex Mono** - Monospace font for code
- **STIX Two Math** - Mathematical symbols

Make sure these fonts are installed on your system or available to your LaTeX distribution.

## Files Included

- `beamerthemeuu.sty` - Main theme file
- `beamercolorthemeuu.sty` - Color definitions
- `beamerinnerthemeuu.sty` - Inner theme (title page, blocks, etc.)
- `beamerouterthemeuu.sty` - Outer theme (header, footer)
- `example.tex` - Example presentation
- `graphics/corner-logo.png` - Sol (sun) logo
- `graphics/circles.png` - Decorative background for closing slide
- `styles/uu-mpl.mplstyle` - Matplotlib style file

## Credits

Utrecht University color palette based on official brand guidelines from https://www.uu.nl/en/organisation/corporate-identity

## License

LPPL 1.3c+
