# Chip

> A versatile chip component for displaying compact information, labels, or status indicators.

## Basic Usage

```html
<!-- Import component -->
<script>
  import { JCChip } from '@lib/Element/Chip/JCChip.svelte';
</script>

<!-- Basic usage -->
<JCChip label="Basic Chip" />
```

## Examples

### Different Variants

```html
<JCChip label="Solid" type="primary" variant="solid" />
<JCChip label="Outline" type="success" variant="outline" />
<JCChip label="Soft" type="warning" variant="soft" />
```

### Different Sizes

```html
<JCChip label="Extra Small" size="xs" />
<JCChip label="Small" size="sm" />
<JCChip label="Base" size="base" />
<JCChip label="Large" size="lg" />
```

### Custom Styling

```html
<JCChip label="Custom" color="bg-purple-500 text-white" />
```

## API

### Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `label` | `string` | 'Chip' | Text content of the chip |
| `type` | `string` | 'primary' | Color theme ('primary', 'secondary', 'success', 'danger', 'warning', 'info', 'light', 'dark') |
| `variant` | `string` | 'solid' | Visual style ('solid', 'outline', 'soft') |
| `size` | `string` | 'sm' | Size of the chip ('xs', 'sm', 'base', 'lg') |
| `disabled` | `boolean` | false | Whether the chip is disabled |
| `rounded` | `boolean` | true | Whether to use rounded corners |
| `color` | `string` | '' | Custom color override using Tailwind classes |

### Slots

| Name | Description |
|------|-------------|
| default | Content that overrides the label prop |

### Usage with Slots

```html
<JCChip>
  Custom content
</JCChip>
```

## Styling

The component uses Tailwind CSS classes for styling and includes:

- Built-in dark mode support
- Customizable through Tailwind classes
- Color variants through the `type` prop
- Visual styles through the `variant` prop
- Size variations
- Custom colors via the `color` prop

### CSS Classes

The component applies these Tailwind CSS classes by default:

```css
/* Base styles */
.jc-chip {
  @apply inline-flex items-center font-medium;
}

/* Size variants */
.jc-chip-xs { @apply px-2 py-0.5 text-xs; }
.jc-chip-sm { @apply px-2 py-0.5 text-sm; }
.jc-chip-base { @apply px-4 py-1 text-base; }
.jc-chip-lg { @apply px-6 py-2 text-lg; }
``` 