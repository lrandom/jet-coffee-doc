# Popover

> A flexible popover component for displaying additional content in an overlay with customizable positioning and styling.

## Basic Usage

```html
<!-- Import component -->
<script>
  import JCPopover from '$lib/Element/Popover/JCPopover.svelte';
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

