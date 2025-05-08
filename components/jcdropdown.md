# Dropdown

> A flexible dropdown menu component with customizable positioning and trigger options.

## Basic Usage

```html
<!-- Import components -->
<script>
  import JCDropdown from '@lib/Element/Dropdown/JCDropdown.svelte';
  import JCDropdownItem from '@lib/Element/Dropdown/JCDropdownItem.svelte';
</script>

<!-- Basic usage -->
<JCDropdown label="Click me">
  <svelte:fragment slot="items">
    <JCDropdownItem>Edit</JCDropdownItem>
    <JCDropdownItem>Delete</JCDropdownItem>
    <JCDropdownItem>Share</JCDropdownItem>
  </svelte:fragment>
</JCDropdown>
```

## Examples

### Custom Trigger

```html
<JCDropdown position="bottom" trigger="hover">
  <button>Hover me</button>
  <svelte:fragment slot="items">
    <JCDropdownItem>Option 1</JCDropdownItem>
    <JCDropdownItem>Option 2</JCDropdownItem>
  </svelte:fragment>
</JCDropdown>
```

### Different Positions

```html
<JCDropdown position="top">Top Dropdown</JCDropdown>
<JCDropdown position="bottom">Bottom Dropdown</JCDropdown>
<JCDropdown position="left">Left Dropdown</JCDropdown>
<JCDropdown position="right">Right Dropdown</JCDropdown>
```

## API

### Props

#### JCDropdown Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `label` | `string` | 'Dropdown' | Button text when using default trigger |
| `position` | `string` | 'bottom' | Dropdown position ('top', 'bottom', 'left', 'right') |
| `trigger` | `string` | 'click' | Trigger type ('click', 'hover') |

#### JCDropdownItem Props

The component accepts all HTML attributes through `$$restProps`.

### Slots

#### JCDropdown Slots

| Name | Description |
|------|-------------|
| default | Trigger element (replaces default button) |
| items | Dropdown menu items |

#### JCDropdownItem Slots

| Name | Description |
|------|-------------|
| default | Content of the dropdown item |

## Features

The dropdown component includes several built-in features:

- 🔄 Automatic positioning to prevent overflow
- 📱 Responsive design with mobile support
- 🌙 Dark mode support
- ⌨️ Keyboard navigation support
- 🖱️ Click outside to close
- 🎯 Custom trigger elements
- 🎨 Customizable styling through Tailwind classes
