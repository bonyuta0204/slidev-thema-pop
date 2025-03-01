# slidev-theme-slidev-thema-pop

[![NPM version](https://img.shields.io/npm/v/slidev-theme-slidev-thema-pop?color=3AB9D4&label=)](https://www.npmjs.com/package/slidev-theme-slidev-thema-pop)

A pop theme for [Slidev](https://github.com/slidevjs/slidev) that provides modern, engaging, and visually appealing presentation layouts and components.

## Features

- 🎨 Modern and clean design
- 🌓 Supports both light and dark modes
- 🧩 Reusable components for creating engaging slides
- 📱 Responsive layouts
- 🔤 Beautiful typography with Nunito Sans and Fira Code fonts

## Install

Add the following frontmatter to your `slides.md`. Start Slidev then it will prompt you to install the theme automatically.

<pre><code>---
theme: <b>slidev-thema-pop</b>
---</code></pre>

Learn more about [how to use a theme](https://sli.dev/guide/theme-addon#use-theme).

## Layouts

This theme provides the following layouts:

- `center`: Centers content both horizontally and vertically

Example usage:

```md
---
layout: center
---

# This slide's content will be centered
```

## Components

This theme provides the following components:

- `Badge`: A highlighted badge that can be positioned in the corner of slides
  ```html
  <Badge>New Feature</Badge>
  ```

- `BoxList`: A grid of visually striking boxes for highlighting key concepts or features
  ```html
  <BoxList :items="['Feature One', 'Feature Two']" :activeIndex="0"/>
  ```

- `MenuList`: A stylish vertical navigation menu for presenting lists of items or topics
  ```html
  <MenuList :items="['Option One', 'Option Two', 'Option Three']" :activeIndex="1"/>
  ```

### BoxList Component

The `BoxList` component creates a responsive grid of visually striking boxes that's ideal for:

- Highlighting key features or concepts
- Presenting comparison points
- Creating visual categorization of topics
- Emphasizing important information with an interactive element

#### Features

- **Responsive Grid Layout**: Automatically adjusts based on the number of items
- **Interactive Highlighting**: Use the `activeIndex` prop to highlight a specific box
- **Elegant Design**: Rounded corners with bold typography for maximum impact
- **Visual Transitions**: Smooth color transitions when highlighting different items
- **Equal Distribution**: Items are automatically sized to fill the available space evenly

#### Props

| Prop | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| `items` | Array<string> | Yes | - | Array of strings to display in the boxes |
| `activeIndex` | Number | No | - | Index of the box to highlight (0-based) |

#### Example Usage

Basic usage with multiple items:
```html
<BoxList :items="['Scalability', 'Security', 'Performance']" />
```

With active item highlighting:
```html
<BoxList 
  :items="['Scalability', 'Security', 'Performance']" 
  :activeIndex="1"
/>
```

Creating a multi-slide sequence with consistent visual elements:
```md
# Security Best Practices

<BoxList :items="[
  'Zero Trust Model',
  'Defense in Depth'
]"/>

---

# Security Best Practices

<BoxList :items="[
  'Zero Trust Model',
  'Defense in Depth'
]" :activeIndex="0"/>
```

This pattern creates a consistent visual theme across slides while drawing attention to different elements as your presentation progresses.

### MenuList Component

The `MenuList` component creates a visually appealing vertical list of items that's perfect for:

- Displaying a table of contents
- Showing a list of topics or categories
- Creating interactive navigation between slide sections
- Highlighting key points in a structured format

#### Features

- **Interactive Highlighting**: Use the `activeIndex` prop to highlight the currently active item
- **Clean Visual Design**: Rounded pill-style items with smooth color transitions
- **Responsive Layout**: Automatically adjusts to fit available space
- **Simple API**: Just provide an array of items and optionally specify which one is active

#### Props

| Prop | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| `items` | Array | Yes | - | Array of strings to display in the menu |
| `activeIndex` | Number | No | - | Index of the item to highlight (0-based) |

#### Example Usage

Basic usage:
```html
<MenuList :items="['Scalability', 'Reliability', 'Security']" />
```

With active item:
```html
<MenuList 
  :items="['Scalability', 'Reliability', 'Security']" 
  :activeIndex="1"
/>
```

Creating a multi-slide sequence (example from the demo):
```md
# Cloud Architecture Pillars

<MenuList :items="[
  'Scalability',
  'Reliability',
  'Security',
  'Cost Optimization',
  'Performance'
]" />

---

# Cloud Architecture Pillars

<MenuList :items="[
  'Scalability',
  'Reliability',
  'Security',
  'Cost Optimization',
  'Performance'
]" :activeIndex="0"/>
```

This creates a consistent visual element across slides, with different items highlighted as you progress through the presentation.


## Example

Check out the `example.md` file in this repository for a complete example presentation that showcases all the features of this theme.

## Contributing

- `pnpm install` to install dependencies
- `pnpm dev` to start theme preview of `example.md`
- Edit the `example.md` and styles to see the changes

## Requirements

- Node.js >= 18.0.0
- [Slidev](https://github.com/slidevjs/slidev) >= 51.3.0

## License
MIT License
