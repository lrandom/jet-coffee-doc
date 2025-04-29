# Tooltip

> A versatile tooltip component that provides contextual information with customizable positioning and styling.

## Basic Usage

```html
<script>
  import { JCTooltip } from '@lib/Element/Tooltip';
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

## Styling

### Default Styles

The component uses Tailwind CSS for styling and includes:

- 🎨 Clean, modern design
- ✨ Smooth fade transitions
- 📏 Proper spacing and padding
- 🎯 Arrow indicators
- 🌙 Dark mode compatibility

### CSS Classes

```css
/* Base tooltip styles */
.jc-tooltip {
  @apply absolute z-50 px-3 py-2 text-sm;
  @apply bg-gray-900 text-white rounded-md shadow-lg;
  @apply dark:bg-gray-700 dark:text-white;
}

/* Arrow styles */
.jc-tooltip-arrow {
  @apply absolute w-2 h-2 bg-gray-900;
  @apply dark:bg-gray-700;
  transform: rotate(45deg);
}

/* Tooltip positions */
.jc-tooltip--top {
  @apply -translate-y-2;
}

.jc-tooltip--bottom {
  @apply translate-y-2;
}

.jc-tooltip--left {
  @apply -translate-x-2;
}

.jc-tooltip--right {
  @apply translate-x-2;
}

/* Fade animation */
.jc-tooltip-fade-enter-active,
.jc-tooltip-fade-leave-active {
  @apply transition-opacity duration-200;
}

.jc-tooltip-fade-enter-from,
.jc-tooltip-fade-leave-to {
  @apply opacity-0;
}
```

### Customization

You can customize the appearance using:
- Different positions through the `position` prop
- Custom width with the `width` prop
- Rich HTML content through slots
- Custom styling through Tailwind classes
- Dark mode support
- Arrow visibility toggle
- Offset adjustment

## Accessibility

The tooltip component follows accessibility best practices:

- Uses appropriate ARIA attributes (`aria-describedby`)
- Keyboard navigation support
- Screen reader friendly
- Focus management
- Role attributes
- Proper contrast ratios 