# List

> A simple and flexible list component for displaying items in a structured format.

## Basic Usage

```html
<!-- Import components -->
<script>
  import JCList from '$lib/Element/List/JCList.svelte';
  import JCListItem from '$lib/Element/List/JCListItem.svelte';
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

