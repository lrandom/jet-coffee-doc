# Progress

> A versatile progress bar component with customizable appearance and label positioning.

## Basic Usage

```html
<!-- Import component -->
<script>
  import JCProgress from '@lib/Element/Progress/JCProgress.svelte';
</script>

<!-- Basic usage -->
<JCProgress progress={60} />
```

## Examples

### Different Types

```html
<JCProgress type="primary" progress={75} />
<JCProgress type="success" progress={80} />
<JCProgress type="warning" progress={40} />
<JCProgress type="danger" progress={90} />
```

### Different Sizes

```html
<JCProgress size="xs" progress={60} />
<JCProgress size="sm" progress={60} />
<JCProgress size="base" progress={60} />
<JCProgress size="lg" progress={60} />
```

### Custom Labels

```html
<!-- Inside label -->
<JCProgress 
  progress={60}
  label="Loading..."
  labelPosition="inside|center"
/>

<!-- Outside label -->
<JCProgress 
  progress={60}
  labelPosition="outside|end"
/>

<!-- Custom colors -->
<JCProgress 
  progress={60}
  color="#ff0000"
  labelColor="red"
/>
```

## API

### Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `type` | `string` | 'primary' | Progress bar type ('primary', 'success', 'warning', 'danger', etc.) |
| `size` | `string` | 'base' | Size of the progress bar ('xs', 'sm', 'base', 'lg') |
| `progress` | `number` | 60 | Progress value (0-100) |
| `label` | `string` | '' | Custom label text |
| `showLabel` | `boolean` | true | Whether to show the label |
| `labelPosition` | `string` | 'inside\|center' | Label position ('inside\|start', 'inside\|center', 'inside\|end', 'outside\|start', 'outside\|center', 'outside\|end') |
| `labelColor` | `string` | 'white' | Color of the label text |
| `color` | `string` | null | Custom background color for the progress bar |

### Slots

| Name | Description |
|------|-------------|
| default | Custom label content |
| label | Custom label content (when using inside position) |

## Features

The progress component includes several built-in features:

- 📏 Multiple size variants
- 🎨 Customizable colors
- 📍 Flexible label positioning
- 📊 Progress percentage display
- 🌙 Dark mode support
- ⭕ Rounded corners
- 📝 Custom label text
- ✨ Smooth transitions

