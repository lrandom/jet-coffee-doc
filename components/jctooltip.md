# Tooltip

> A versatile tooltip component that provides contextual information with customizable positioning and styling.

## Basic Usage

```html
<script>
  import JCTooltip from '@lib/Element/Tooltip/JCTooltip.svelte';
</script>

<!-- Basic usage -->
<JCTooltip content="This is a tooltip">
  <button>Hover me</button>
</JCTooltip>
```

## Examples

### Different Positions
```html
<JCTooltip content="Top tooltip" position="top">
  <button>Hover for top tooltip</button>
</JCTooltip>

<JCTooltip content="Bottom tooltip" position="bottom">
  <button>Hover for bottom tooltip</button>
</JCTooltip>

<JCTooltip content="Left tooltip" position="left">
  <button>Hover for left tooltip</button>
</JCTooltip>

<JCTooltip content="Right tooltip" position="right">
  <button>Hover for right tooltip</button>
</JCTooltip>
```

### Custom Width and HTML Content

```html
<JCTooltip width="300px">
  <div slot="content">
    <h3>Custom HTML Content</h3>
    <p>This tooltip contains <strong>formatted</strong> content.</p>
  </div>
  <button>Hover for rich content</button>
</JCTooltip>
```

### Show/Hide on Click

```html
<JCTooltip trigger="click" content="Click-triggered tooltip">
  <button>Click me</button>
</JCTooltip>
```

## API

### Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `content` | `string` | - | Text content for the tooltip |
| `position` | `string` | 'top' | Tooltip position ('top', 'bottom', 'left', 'right') |
| `trigger` | `string` | 'hover' | Trigger type ('hover', 'click') |
| `width` | `string` | 'auto' | Custom width for the tooltip |
| `delay` | `number` | 0 | Delay in ms before showing tooltip |
| `arrow` | `boolean` | true | Whether to show the arrow pointer |
| `disabled` | `boolean` | false | Disable the tooltip |
| `offset` | `number` | 8 | Distance between tooltip and trigger element |

### Slots

| Name | Description |
|------|-------------|
| default | Trigger element that the tooltip will be attached to |
| content | Custom HTML content for the tooltip |

### Events

| Name | Description |
|------|-------------|
| `show` | Fired when tooltip is shown |
| `hide` | Fired when tooltip is hidden |

## Features

The tooltip component includes several built-in features:

- 🎯 Multiple positioning options
- 🖱️ Click and hover triggers
- 📏 Customizable width
- ⏱️ Show/hide delay
- 🎨 Custom HTML content support
- 🏹 Optional arrow pointer
- 🔄 Auto-positioning
- 🌙 Dark mode support
- ⌨️ Keyboard accessibility
- 📱 Mobile-friendly

