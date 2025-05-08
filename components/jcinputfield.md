# Input Field

> A versatile input field component with support for different types, states, and validation.

## Basic Usage

```html
<script>
  import { JCInputField } from '@lib/Form/InputField/JCInputField.svelte';
  let value = '';
</script>

<!-- Basic usage -->
<JCInputField
  bind:value
  label="Username"
  placeholder="Enter your username"
/>
```

## Examples

### Different Types

```html
<!-- Text input -->
<JCInputField type="text" label="Text Input" />

<!-- Password input -->
<JCInputField type="password" label="Password" />

<!-- Email input -->
<JCInputField type="email" label="Email Address" />

<!-- Number input -->
<JCInputField type="number" label="Age" />
```

### Different States

```html
<!-- With placeholder -->
<JCInputField placeholder="Enter value..." />

<!-- With helper text -->
<JCInputField helperText="This is a helper text" />

<!-- With error -->
<JCInputField error="This field is required" />

<!-- Disabled state -->
<JCInputField disabled value="Disabled input" />

<!-- Read-only state -->
<JCInputField readonly value="Read-only input" />
```

### With Icons

```html
<JCInputField
  label="Search"
  leftIcon="search"
  placeholder="Search..."
/>

<JCInputField
  label="Password"
  rightIcon="eye"
  type="password"
/>
```

## API

### Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `value` | `string` | '' | Input value |
| `type` | `string` | 'text' | Input type (text, password, email, etc.) |
| `label` | `string` | undefined | Label text |
| `placeholder` | `string` | undefined | Placeholder text |
| `disabled` | `boolean` | false | Whether the input is disabled |
| `readonly` | `boolean` | false | Whether the input is read-only |
| `required` | `boolean` | false | Whether the input is required |
| `error` | `string` | undefined | Error message |
| `helperText` | `string` | undefined | Helper text |
| `leftIcon` | `string` | undefined | Icon to show on the left |
| `rightIcon` | `string` | undefined | Icon to show on the right |
| `size` | `string` | 'base' | Input size ('sm', 'base', 'md', 'lg') |

### Events

| Name | Description |
|------|-------------|
| `input` | Fired when input value changes |
| `focus` | Fired when input receives focus |
| `blur` | Fired when input loses focus |
| `change` | Fired when input value is committed |

### Slots

| Name | Description |
|------|-------------|
| leftIcon | Custom left icon content |
| rightIcon | Custom right icon content |
| error | Custom error message content |
| helper | Custom helper text content |

## Features

- 📝 Multiple input types
- 🎨 Customizable appearance
- ⚠️ Error state handling
- 💡 Helper text support
- 🔍 Icon integration
- ⌨️ Keyboard support
- 📱 Responsive design
- 🌙 Dark mode support

## Styling

### Default Styles

```css
/* Base input styles */
.jc-input {
  @apply w-full rounded-md border-gray-300;
  @apply focus:ring-primary-500 focus:border-primary-500;
  @apply dark:bg-gray-700 dark:border-gray-600;
}

/* Label styles */
.jc-input__label {
  @apply block text-sm font-medium text-gray-700;
  @apply dark:text-gray-200;
}

/* Error state */
.jc-input--error {
  @apply border-red-500;
  @apply focus:ring-red-500 focus:border-red-500;
}

/* Helper text */
.jc-input__helper {
  @apply mt-1 text-sm text-gray-500;
  @apply dark:text-gray-400;
}

/* Error message */
.jc-input__error {
  @apply mt-1 text-sm text-red-500;
}

/* Icon container */
.jc-input__icon {
  @apply absolute inset-y-0 flex items-center;
  @apply text-gray-400 dark:text-gray-500;
}
```

### Customization

You can customize the appearance using:
- Different input types
- Custom icons through slots
- Error and helper text styling
- Size variants
- Dark mode support
- Custom Tailwind classes

## Accessibility

The input field component follows accessibility best practices:

- Proper label association
- ARIA attributes for states
- Error message announcements
- Keyboard navigation
- Focus management
- Screen reader support 