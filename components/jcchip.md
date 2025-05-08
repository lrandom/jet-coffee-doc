# Chip

> A versatile chip component for displaying compact information, labels, or status indicators.

## Basic Usage

```html
<!-- Import component -->
<script>
  import JCChip from '@lib/Element/Chip/JCChip.svelte';
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

