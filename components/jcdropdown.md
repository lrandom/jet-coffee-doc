# Dropdown

> A flexible dropdown menu component with customizable positioning and trigger options.

## Basic Usage

```html
<!-- Import components -->
<script>
  import { JCDropdown, JCDropdownItem } from '@lib/Element/Dropdown';
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

## Styling

### CSS Classes

The component applies these Tailwind CSS classes by default:

```css
/* Base dropdown styles */
.jc-dropdown {
  @apply relative;
}

/* Dropdown content wrapper */
.jc-dropdown-content {
  @apply absolute min-w-[10rem] w-fit bg-white dark:bg-gray-800 rounded-md shadow-md overflow-hidden z-50;
}

/* Dark mode border */
.dark .jc-dropdown-content {
  @apply border border-gray-700;
}
```

### Customization

You can customize the appearance using:
- Custom trigger elements through the default slot
- Additional Tailwind classes through the class prop
- Dark mode styles are automatically applied
- Position customization through the `position` prop 