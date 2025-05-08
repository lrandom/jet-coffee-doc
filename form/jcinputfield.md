# Input Field

> A versatile input field component with support for different types, states, and validation.

## Basic Usage

```html
<script>
  import JCInputField from '$lib/Form/InputField/JCInputField.svelte';
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

### With Prefix

```html
<JCInputField
  label="Price"
  prefix="$"
  type="number"
  placeholder="0.00"
/>

<JCInputField
  label="Website"
  prefix="https://"
  placeholder="example.com"
/>
```

### With Slot Prefix/Suffix

```html
<JCInputField label="Currency" prefix={true} suffix={true}>
		<svelte:fragment slot="prefix">
		  <select class="border-none bg-transparent pr-1">
			<option>$</option>
			<option>€</option>
			<option>£</option>
		  </select>
		</svelte:fragment>
		<svelte:fragment slot="suffix">
		  <span class="text-gray-500">USD</span>
		</svelte:fragment>
	  </JCInputField>
	  
	  <JCInputField label="Weight" suffix={true}>
		<div slot="suffix" class="flex items-center">
		  <select class="border-none bg-transparent">
			<option>kg</option>
			<option>lb</option>
			<option>g</option>
		  </select>
		</div>
	  </JCInputField>
```

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
| `prefix` | `string` | undefined | Text prefix displayed before the input value |
| `suffix` | `string` | undefined | Text suffix displayed after the input value |
| `size` | `string` | 'base' | Input size ('sm', 'base', 'lg') |

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
| prefix | Custom prefix content |
| suffix | Custom suffix content |
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


## Accessibility

The input field component follows accessibility best practices:

- Proper label association
- ARIA attributes for states
- Error message announcements
- Keyboard navigation
- Focus management
- Screen reader support 