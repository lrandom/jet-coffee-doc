# Breadcrumb Component

The JCBreadcrumb component provides navigation context by showing the current location within a navigational hierarchy.

## Basic Usage

```svelte
<script>
  import JCBreadcrumb from '$lib/Element/Breadcrumb/JCBreadcrumb.svelte';
</script>

<JCBreadcrumb
  items={[
    { content: 'Home', href: '/' },
    { content: 'Products', href: '/products' },
    { content: 'Details' }
  ]}
  border={true}
/>
```

## Props

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| items | BreadcrumbItem[] | [...] | Array of breadcrumb items |
| border | boolean | false | Adds border and shadow to breadcrumb |

## Features

- Automatic chevron separators
- Support for both links and text items
- Dark mode support
- Optional bordered style
- HTML content support in items
- Customizable link targets
