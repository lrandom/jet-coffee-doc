# Radio

> A customizable radio button component for single selection from a group of options.

## Basic Usage

```html
<script>
  import { JCRadio } from '@lib/Form/Radio';
  let selected = 'option1';
</script>

<!-- Basic usage -->
<JCRadio
  bind:group={selected}
  value="option1"
>
  Option 1
</JCRadio>
<JCRadio
  bind:group={selected}
  value="option2"
>
  Option 2
</JCRadio>
```

## Examples

### Different Sizes

```html
<JCRadio size="sm">Small radio</JCRadio>
<JCRadio size="base">Base radio</JCRadio>
<JCRadio size="lg">Large radio</JCRadio>
```

### Radio Group

```html
<script>
  let selectedValue = 'apple';
  const options = [
    { value: 'apple', label: 'Apple' },
    { value: 'banana', label: 'Banana' },
    { value: 'orange', label: 'Orange' }
  ];
</script>

<JCRadio.Group
  bind:value={selectedValue}
  options={options}
  name="fruits"
/>
```

### Custom Styling

```html
<JCRadio class="custom-radio" color="success">
  Custom styled radio
</JCRadio>
```

### Disabled State

```html
<JCRadio disabled>Disabled option</JCRadio>
```

## API

### Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `value` | `any` | undefined | Radio button value |
| `group` | `any` | undefined | Selected value in the group |
| `name` | `string` | undefined | Name attribute for the input |
| `disabled` | `boolean` | false | Whether the radio is disabled |
| `size` | `string` | 'base' | Size of the radio ('sm', 'base', 'lg') |
| `color` | `string` | 'primary' | Color theme of the radio |
| `required` | `boolean` | false | Whether the radio is required |

### Events

| Name | Description |
|------|-------------|
| `change` | Fired when selection changes |
| `focus` | Fired when radio receives focus |
| `blur` | Fired when radio loses focus |

### Slots

| Name | Description |
|------|-------------|
| default | Label content |

## Features

- 🎯 Single selection
- 📏 Multiple sizes
- 🎨 Color themes
- 👥 Group functionality
- ⌨️ Keyboard navigation
- 🌙 Dark mode support
- ♿ Accessibility features
- 📱 Touch friendly

## Styling

### Default Styles

```css
/* Base radio styles */
.jc-radio {
  @apply relative inline-flex items-center;
}

/* Radio input */
.jc-radio__input {
  @apply w-4 h-4 text-primary-600;
  @apply border-gray-300 focus:ring-primary-500;
  @apply dark:border-gray-600 dark:bg-gray-700;
}

/* Size variants */
.jc-radio--sm {
  @apply text-sm;
  .jc-radio__input { @apply w-3 h-3; }
}

.jc-radio--lg {
  @apply text-lg;
  .jc-radio__input { @apply w-5 h-5; }
}

/* Color variants */
.jc-radio--primary .jc-radio__input { @apply text-primary-500; }
.jc-radio--success .jc-radio__input { @apply text-success-500; }
.jc-radio--warning .jc-radio__input { @apply text-warning-500; }
.jc-radio--danger .jc-radio__input { @apply text-danger-500; }

/* Disabled state */
.jc-radio--disabled {
  @apply opacity-50 cursor-not-allowed;
}

/* Focus state */
.jc-radio__input:focus {
  @apply ring-2 ring-offset-2;
}

/* Radio group */
.jc-radio-group {
  @apply space-y-2;
}

.jc-radio-group--horizontal {
  @apply flex space-x-4 space-y-0;
}
```

### Customization

You can customize the appearance using:
- Different sizes through the `size` prop
- Color themes through the `color` prop
- Custom styles through Tailwind classes
- Group layout options
- Dark mode support
- Focus styles

## Accessibility

The radio component follows accessibility best practices:

- Uses native `<input type="radio">` element
- Proper grouping with fieldset and legend
- Keyboard navigation
- Focus management
- State announcements
- Touch target sizing
- High contrast support 