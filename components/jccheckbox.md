# Checkbox

> A customizable checkbox component with support for different states, sizes, and grouping.

## Basic Usage

```html
<script>
  import { JCCheckbox } from '@lib/Form/Checkbox.svelte';
  let checked = false;
</script>

<!-- Basic usage -->
<JCCheckbox bind:checked>
  Accept terms and conditions
</JCCheckbox>
```

## Examples

### Different States

```html
<!-- Default state -->
<JCCheckbox>Default checkbox</JCCheckbox>

<!-- Checked state -->
<JCCheckbox checked>Checked checkbox</JCCheckbox>

<!-- Disabled state -->
<JCCheckbox disabled>Disabled checkbox</JCCheckbox>

<!-- Indeterminate state -->
<JCCheckbox indeterminate>Indeterminate checkbox</JCCheckbox>
```

### Different Sizes

```html
<JCCheckbox size="sm">Small checkbox</JCCheckbox>
<JCCheckbox size="base">Base checkbox</JCCheckbox>
<JCCheckbox size="lg">Large checkbox</JCCheckbox>
```

### Checkbox Group

```html
<script>
  let selectedItems = ['option1'];
</script>

<JCCheckbox.Group bind:value={selectedItems}>
  <JCCheckbox value="option1">Option 1</JCCheckbox>
  <JCCheckbox value="option2">Option 2</JCCheckbox>
  <JCCheckbox value="option3">Option 3</JCCheckbox>
</JCCheckbox.Group>
```

## Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `checked` | `boolean` | false | Whether the checkbox is checked |
| `disabled` | `boolean` | false | Whether the checkbox is disabled |
| `indeterminate` | `boolean` | false | Whether the checkbox is in indeterminate state |
| `size` | `string` | 'base' | Size of the checkbox ('sm', 'base', 'lg') |
| `value` | `any` | undefined | Value for checkbox when used in a group |
| `name` | `string` | undefined | Name attribute for the input element |
| `required` | `boolean` | false | Whether the checkbox is required |

## Events

| Name | Description |
|------|-------------|
| `change` | Fired when checkbox state changes |
| `focus` | Fired when checkbox receives focus |
| `blur` | Fired when checkbox loses focus |

## Slots

| Name | Description |
|------|-------------|
| default | Content next to the checkbox |

## Features

- ✅ Multiple sizes
- 🎨 Customizable appearance
- 🔄 Indeterminate state support
- 👥 Group functionality
- ⌨️ Keyboard navigation
- ♿ Accessibility support
- 🌙 Dark mode compatibility

## Styling

### Default Styles

```css
/* Base checkbox styles */
.jc-checkbox {
  @apply relative inline-flex items-center;
}

/* Checkbox input */
.jc-checkbox__input {
  @apply w-4 h-4 text-primary-600 rounded;
  @apply border-gray-300 focus:ring-primary-500;
  @apply dark:border-gray-600 dark:bg-gray-700;
}

/* Size variants */
.jc-checkbox--sm { @apply text-sm; }
.jc-checkbox--base { @apply text-base; }
.jc-checkbox--lg { @apply text-lg; }

/* Disabled state */
.jc-checkbox--disabled {
  @apply opacity-50 cursor-not-allowed;
}
```

### Customization

You can customize the appearance using:
- Different sizes through the `size` prop
- Custom styles through Tailwind classes
- Dark mode support
- Group layout options

## Accessibility

The checkbox component follows accessibility best practices:

- Uses native `<input type="checkbox">` element
- Proper ARIA attributes
- Keyboard navigation support
- Focus management
- Screen reader friendly 