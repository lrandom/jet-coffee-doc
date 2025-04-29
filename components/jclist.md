# List

> A simple and flexible list component for displaying items in a structured format.

## Basic Usage

```html
<!-- Import components -->
<script>
  import { JCList, JCListItem } from '@lib/Element/List';
</script>

<!-- Basic unordered list -->
<JCList>
  <JCListItem>First item</JCListItem>
  <JCListItem>Second item</JCListItem>
  <JCListItem>Third item</JCListItem>
</JCList>
```

## Examples

### Ordered List

```html
<JCList tag="ol">
  <JCListItem>Step 1</JCListItem>
  <JCListItem>Step 2</JCListItem>
  <JCListItem>Step 3</JCListItem>
</JCList>
```

### Custom Styling

```html
<JCList class="bg-gray-100 p-4">
  <JCListItem class="hover:bg-gray-200">
    Hoverable item
  </JCListItem>
</JCList>
```

## API

### Props

#### JCList Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `tag` | `string` | 'ul' | HTML tag to use ('ul' or 'ol') |

#### JCListItem Props

The component accepts all HTML attributes through `$$restProps`.

### Slots

#### JCList Slots

| Name | Description |
|------|-------------|
| default | List items |

#### JCListItem Slots

| Name | Description |
|------|-------------|
| default | Content of the list item |

## Features

The list component includes several built-in features:

- 📝 Support for both ordered and unordered lists
- 🎨 Customizable through Tailwind classes
- 🌙 Dark mode support
- 📜 Scrollable with custom scrollbar styling
- ♿ Accessible with proper ARIA roles
- 🔄 Flexible content structure through slots

## Styling

### Default Styles

The component includes these default features:

- ⭕ Rounded corners
- 📏 Proper spacing between items
- 📜 Custom scrollbar styling
- 🌙 Dark mode compatibility
- ⚡ Overflow handling

### CSS Classes

The component applies these Tailwind CSS classes by default:

```css
/* Base list styles */
.jc-list-group {
  @apply rounded-md space-y-4 py-4 overflow-y-auto overflow-x-hidden;
}

/* Dark mode styles */
.dark .jc-list-group {
  @apply bg-gray-800 text-gray-200;
}

/* Custom scrollbar */
.jc-beauty-scrollbar {
  @apply scrollbar-thin scrollbar-thumb-gray-400 dark:scrollbar-thumb-gray-600;
}
```

### Customization

You can customize the appearance using:
- The `tag` prop for list type
- Additional Tailwind classes through the class prop
- Dark mode styles are automatically applied
- Custom scrollbar styling through the `.jc-beauty-scrollbar` class 