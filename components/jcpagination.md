# Pagination

> A comprehensive pagination component for handling page navigation with various styles and configurations.

## Basic Usage

```html
<!-- Import component -->
<script>
  import JCPagination from '@lib/Element/Pagination/JCPagination';
  let currentPage = 1;
</script>

<!-- Basic usage -->
<JCPagination 
  bind:activePage={currentPage}
  totalPage={10}
/>
```

## Examples

### Different Shapes

```html
<JCPagination shape="rounded" />
<JCPagination shape="circle" />
<JCPagination shape="square" />
```

### Different Sizes

```html
<JCPagination size="xs" />
<JCPagination size="sm" />
<JCPagination size="base" />
<JCPagination size="lg" />
<JCPagination size="xl" />
```

### Custom Visible Pages

```html
<JCPagination 
  totalPage={20}
  totalVisible={3}
/>
```

### Disabled State

```html
<JCPagination disabled />
```

## API

### Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `shape` | `string` | 'rounded' | Shape of pagination items ('rounded', 'circle', 'square') |
| `size` | `string` | 'base' | Size of pagination items ('xs', 'sm', 'base', 'lg', 'xl') |
| `activeClass` | `string` | '!bg-primary !text-white' | Class applied to active page item |
| `disabled` | `boolean` | false | Whether the pagination is disabled |
| `activePage` | `number` | 1 | Current active page number |
| `totalPage` | `number` | 15 | Total number of pages |
| `totalVisible` | `number` | 2 | Number of visible page items (excluding prev/next) |
| `tag` | `string` | 'button' | HTML tag for pagination items |

## Features

The pagination component includes several built-in features:

- 🎨 Multiple shape variants
- 📏 Responsive sizing options
- 🎯 Customizable active page styling
- 📱 Dynamic page number display
- ⬅️ Previous/Next navigation
- ⚡ Disabled state support
- 📱 Touch swipe support for mobile
- ⌨️ Keyboard navigation
- 🔄 Automatic overflow handling
- 🌙 Dark mode support
