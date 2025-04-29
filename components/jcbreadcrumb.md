# Breadcrumb Component

The JCBreadcrumb component provides navigation context by showing the current location within a navigational hierarchy.

## Props

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| items | BreadcrumbItem[] | [...] | Array of breadcrumb items |
| border | boolean | false | Adds border and shadow to breadcrumb |

## Types

```typescript
type BreadcrumbItem = {
  content: string;   // Text content
  href?: string;     // Optional link URL
  target?: string;   // Optional link target
}
```

## Features

- Automatic chevron separators
- Support for both links and text items
- Dark mode support
- Optional bordered style
- HTML content support in items
- Customizable link targets

## Example

```svelte
<JCBreadcrumb
  items={[
    { content: 'Home', href: '/' },
    { content: 'Products', href: '/products' },
    { content: 'Details' }
  ]}
  border={true}
/>
```

## Styling

- Active links: Blue with hover state
- Current item: Gray text
- Separators: Gray chevron icons
- Optional border and shadow
- Responsive layout 