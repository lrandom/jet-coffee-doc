# Tabs

> A comprehensive tabbed interface component for organizing content with support for different styles and layouts.

## Basic Usage

```html
<!-- Import components -->
<script>
  import { JCTabs, JCTabItem } from '@lib/Element/Tab';
</script>

<!-- Basic usage -->
<JCTabs>
  <JCTabItem label="Tab 1">
    Content for tab 1
  </JCTabItem>
  <JCTabItem label="Tab 2">
    Content for tab 2
  </JCTabItem>
</JCTabs>
```

## Examples

### Different Types

```html
<JCTabs type="default">Default Tabs</JCTabs>
<JCTabs type="pill">Pill Tabs</JCTabs>
```

### Full Width Tabs

```html
<JCTabs fullTab>
  <JCTabItem label="Full Width Tab">
    Content spans full width
  </JCTabItem>
</JCTabs>
```

### Separated Content

```html
<JCTabs separated>
  <svelte:fragment slot="items">
    <JCTabItem label="Tab 1" />
    <JCTabItem label="Tab 2" />
  </svelte:fragment>
  <svelte:fragment slot="content">
    <div>Content for active tab</div>
  </svelte:fragment>
</JCTabs>
```

### Programmatic Control

```html
<script>
  let activeTabId = 'tab1';
</script>

<JCTabs bind:activeTabId>
  <JCTabItem id="tab1" label="Tab 1">
    Content 1
  </JCTabItem>
  <JCTabItem id="tab2" label="Tab 2">
    Content 2
  </JCTabItem>
</JCTabs>
```

## API

### Props

#### JCTabs Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `fullTab` | `boolean` | false | Whether tabs should take full width |
| `type` | `string` | 'default' | Tab style type ('default', 'pill') |
| `separated` | `boolean` | false | Whether to separate tab items from content |
| `activeTabId` | `string \| null` | null | ID of the active tab |

#### JCTabItem Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `label` | `string` | - | Label text for the tab |
| `id` | `string` | - | Unique identifier for the tab |

### Slots

#### JCTabs Slots

| Name | Description |
|------|-------------|
| default | Tab items (when not using separated mode) |
| items | Tab items (when using separated mode) |
| content | Tab content (when using separated mode) |

#### JCTabItem Slots

| Name | Description |
|------|-------------|
| default | Content for the tab panel |

### Methods

| Name | Description |
|------|-------------|
| `setActiveTab(id: string)` | Programmatically set the active tab |

## Features

The tabs component includes several built-in features:

- 🎨 Multiple tab styles (default and pill)
- 📏 Full width tabs option
- 🔄 Separated content mode
- 🎯 Programmatic control
- 📱 Mobile-responsive design
- 📱 Touch swipe support
- ⌨️ Keyboard navigation
- ♾️ Automatic overflow handling
- 🌙 Dark mode support

## Styling

### Default Styles

The component uses Tailwind CSS for styling and includes:

- 🎨 Clean, modern design
- ✨ Smooth transitions
- 📏 Proper spacing and padding
- 🎯 Active tab indicators
- 🌙 Dark mode compatibility
- 📱 Mobile-responsive layout

### CSS Classes

```css
/* Base tab styles */
.jc-tab {
  @apply bg-white dark:bg-gray-800 rounded-lg;
}

/* Tab navigation */
.jc-tab-nav {
  @apply flex items-center space-x-2 px-4 py-2;
}

/* Tab item */
.jc-tab-item {
  @apply px-4 py-2 rounded-md cursor-pointer;
  @apply hover:bg-gray-100 dark:hover:bg-gray-700;
}

/* Active tab */
.jc-tab-item--active {
  @apply bg-primary text-white;
  @apply dark:bg-primary dark:text-white;
}

/* Tab content */
.jc-tab-content {
  @apply p-4;
}

/* Pill variant */
.jc-tab--pill {
  @apply bg-gray-50 dark:bg-gray-700;
}
```

### Customization

You can customize the appearance using:
- Different tab types through the `type` prop
- Full width tabs with `fullTab`
- Custom styling through Tailwind classes
- Separated content layout
- Custom tab content through slots
- Mobile-responsive behavior
- Touch gesture support 