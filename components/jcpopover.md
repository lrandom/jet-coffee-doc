# Popover

> A flexible popover component for displaying additional content in an overlay with customizable positioning and styling.

## Basic Usage

```html
<!-- Import component -->
<script>
  import { JCPopover } from '@lib/Element/Popover';
</script>

<!-- Basic usage -->
<JCPopover>
  <button>Click me</button>
  <svelte:fragment slot="title">
    Popover Title
  </svelte:fragment>
  <svelte:fragment slot="content">
    This is the popover content.
  </svelte:fragment>
</JCPopover>
```

## Examples

### Different Positions

```html
<JCPopover position="top">Top Popover</JCPopover>
<JCPopover position="bottom">Bottom Popover</JCPopover>
<JCPopover position="start">Start Popover</JCPopover>
<JCPopover position="end">End Popover</JCPopover>
```

### Custom Width

```html
<JCPopover width="300px">Wide Popover</JCPopover>
```

### Without Close Button

```html
<JCPopover showCloseButton={false}>No Close Button</JCPopover>
```

### Without Arrow

```html
<JCPopover arrow={false}>No Arrow</JCPopover>
```

## API

### Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `position` | `string` | 'bottom' | Popover position ('top', 'bottom', 'start', 'end') |
| `closeOnClickOutside` | `boolean` | true | Whether to close when clicking outside |
| `width` | `string` | '200px' | Width of the popover |
| `showCloseButton` | `boolean` | true | Whether to show the close button |
| `arrow` | `boolean` | true | Whether to show the arrow pointer |

### Slots

| Name | Description |
|------|-------------|
| default | Trigger element |
| title | Popover header content |
| content | Main popover content |

## Features

The popover component includes several built-in features:

- 🎯 Multiple positioning options
- 🖱️ Click outside to close
- 📏 Customizable width
- ❌ Optional close button
- ➡️ Optional arrow pointer
- 🔄 Automatic positioning adjustment
- ✨ Smooth fade transition
- ⌨️ Keyboard navigation (Escape to close)
- 🌙 Dark mode support

## Styling

### Default Styles

The component uses Tailwind CSS for styling and includes:

- 🎨 Clean, modern design
- ✨ Smooth transitions
- 📏 Proper spacing and padding
- 🌫️ Shadow effects
- 🎯 Border styling
- 🌙 Dark mode compatibility

### CSS Classes

```css
/* Base popover styles */
.jc-popover {
  @apply absolute bg-white rounded-xl shadow-[0_4px_20px_rgba(0,0,0,0.1)] border border-gray-100;
  backdrop-filter: blur(8px);
}

/* Dark mode styles */
.dark .jc-popover {
  @apply bg-gray-800 border-gray-700;
}

/* Arrow styles */
.popover-arrow {
  @apply absolute w-4 h-4 bg-white border border-gray-100;
  box-shadow: -2px -2px 4px rgba(0,0,0,0.03);
}
```

### Customization Options

You can customize the appearance using:
- Width through the `width` prop
- Custom content through slots
- Additional Tailwind classes
- Arrow positioning and styling
- Background blur effect

## Accessibility

The component includes several accessibility features:

- ♿ Proper ARIA attributes
- ⌨️ Keyboard navigation support
- 🔍 Focus management
- 📢 Screen reader friendly structure 