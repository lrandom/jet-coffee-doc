# Progress

> A versatile progress bar component with customizable appearance and label positioning.

## Basic Usage

```html
<!-- Import component -->
<script>
  import { JCProgress } from '@lib/Element/Progress';
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

## Styling

### Default Styles

The component uses Tailwind CSS for styling and includes:

- 🎨 Clean, modern design
- 📏 Proper spacing and padding
- ⭕ Rounded corners
- 🌙 Dark mode compatibility
- 🎯 Custom color support

### CSS Classes

```css
/* Base progress styles */
.jc-progress {
  @apply relative bg-gray-200 dark:bg-gray-700 overflow-hidden w-full;
}

/* Size variants */
.jc-progress-xs { @apply h-2 rounded-xl; }
.jc-progress-sm { @apply h-3 rounded-xl; }
.jc-progress-base { @apply h-4 rounded-xl; }
.jc-progress-lg { @apply h-5 rounded-xl; }

/* Label styles */
.jc-progress-label {
  @apply absolute inset-0 flex items-center px-2;
}

/* Dark mode bar */
.dark .jc-progress-bar {
  @apply bg-primary dark:bg-primary;
}
```

### Customization

You can customize the appearance using:
- The `type` prop for predefined colors
- The `color` prop for custom colors
- The `labelColor` prop for label styling
- Additional Tailwind classes through the class prop
- Label positioning through the `labelPosition` prop 