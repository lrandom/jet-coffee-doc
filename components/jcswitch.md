# Switch

> A toggle switch component for boolean input with customizable styling and labels.

## Basic Usage

```html
<script>
  import { JCSwitch } from '@lib/Form/Switch';
  let checked = false;
</script>

<!-- Basic usage -->
<JCSwitch bind:checked />
```

## Examples

### With Labels

```html
<JCSwitch>
  Enable notifications
</JCSwitch>
```

### Different Sizes

```html
<JCSwitch size="sm">Small switch</JCSwitch>
<JCSwitch size="base">Base switch</JCSwitch>
<JCSwitch size="lg">Large switch</JCSwitch>
```

### Custom Colors

```html
<JCSwitch color="success">Success switch</JCSwitch>
<JCSwitch color="warning">Warning switch</JCSwitch>
<JCSwitch color="danger">Danger switch</JCSwitch>
```

### With Icons

```html
<JCSwitch>
  <svelte:fragment slot="checked-icon">✓</svelte:fragment>
  <svelte:fragment slot="unchecked-icon">✗</svelte:fragment>
  Toggle with icons
</JCSwitch>
```

## API

### Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `checked` | `boolean` | false | Whether the switch is checked |
| `disabled` | `boolean` | false | Whether the switch is disabled |
| `size` | `string` | 'base' | Size of the switch ('sm', 'base', 'lg') |
| `color` | `string` | 'primary' | Color theme ('primary', 'success', 'warning', 'danger') |
| `name` | `string` | undefined | Name attribute for the input |
| `required` | `boolean` | false | Whether the switch is required |
| `value` | `any` | undefined | Value attribute for the input |

### Events

| Name | Description |
|------|-------------|
| `change` | Fired when switch state changes |
| `focus` | Fired when switch receives focus |
| `blur` | Fired when switch loses focus |

### Slots

| Name | Description |
|------|-------------|
| default | Label content |
| checked-icon | Icon for checked state |
| unchecked-icon | Icon for unchecked state |

## Features

- 🎨 Multiple color themes
- 📏 Different sizes
- 🔄 Smooth transitions
- 🖼️ Custom icons
- ⌨️ Keyboard support
- 🌙 Dark mode support
- ♿ Accessibility features
- 📱 Touch friendly

## Styling

### Default Styles

```css
/* Base switch styles */
.jc-switch {
  @apply relative inline-flex items-center;
}

/* Switch track */
.jc-switch__track {
  @apply w-11 h-6 bg-gray-200 rounded-full;
  @apply dark:bg-gray-700;
  @apply transition-colors duration-200;
}

/* Switch thumb */
.jc-switch__thumb {
  @apply absolute w-5 h-5 bg-white rounded-full;
  @apply transform transition-transform duration-200;
  @apply shadow-sm;
}

/* Checked state */
.jc-switch--checked .jc-switch__track {
  @apply bg-primary-500;
}

.jc-switch--checked .jc-switch__thumb {
  @apply translate-x-5;
}

/* Size variants */
.jc-switch--sm {
  .jc-switch__track { @apply w-8 h-4; }
  .jc-switch__thumb { @apply w-3 h-3; }
}

.jc-switch--lg {
  .jc-switch__track { @apply w-14 h-8; }
  .jc-switch__thumb { @apply w-7 h-7; }
}

/* Color variants */
.jc-switch--success .jc-switch__track { @apply bg-success-500; }
.jc-switch--warning .jc-switch__track { @apply bg-warning-500; }
.jc-switch--danger .jc-switch__track { @apply bg-danger-500; }

/* Disabled state */
.jc-switch--disabled {
  @apply opacity-50 cursor-not-allowed;
}

/* Focus state */
.jc-switch:focus-within .jc-switch__track {
  @apply ring-2 ring-offset-2 ring-primary-500;
}
```

### Customization

You can customize the appearance using:
- Different sizes through the `size` prop
- Color themes through the `color` prop
- Custom icons in slots
- Dark mode support
- Track and thumb styling
- Animation timing
- Focus styles

## Accessibility

The switch component follows accessibility best practices:

- Uses native `<input type="checkbox">` under the hood
- Proper ARIA switch role
- Keyboard navigation
- Focus management
- State announcements
- Touch target sizing
- High contrast support 