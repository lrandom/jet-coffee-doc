# Tabs

> A comprehensive tabbed interface component for organizing content with support for different styles and layouts.

## Basic Usage

```html
<!-- Import components -->
<script>
  import JCTabs from '@lib/Element/Tab';
  import JCTabItem from '@lib/Element/Tab';
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

### Using JCTabContent Component

```html
<script>
  import JCTabs from '@lib/Element/Tab/JCTabs.svelte';
  import JCTabItem from '@lib/Element/Tab/JCTabItem.svelte';
  import JCTabContent from '@lib/Element/Tab/JCTabContent.svelte';
</script>

<JCTabs separated>
  <svelte:fragment slot="items">
    <JCTabItem id="tab1" label="First Tab" />
    <JCTabItem id="tab2" label="Second Tab" />
    <JCTabItem id="tab3" label="Third Tab" />
  </svelte:fragment>
  
  <svelte:fragment slot="content">
    <JCTabContent id="tab1">
      <h3>Content for First Tab</h3>
      <p>This content is shown when the first tab is active.</p>
    </JCTabContent>
    
    <JCTabContent id="tab2">
      <h3>Content for Second Tab</h3>
      <p>This content is shown when the second tab is active.</p>
    </JCTabContent>
    
    <JCTabContent id="tab3">
      <h3>Content for Third Tab</h3>
      <p>This content is shown when the third tab is active.</p>
    </JCTabContent>
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

#### JCTabContent Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `id` | `string` | - | Unique identifier matching a tab item |

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

#### JCTabContent Slots

| Name | Description |
|------|-------------|
| default | Content to show when the associated tab is active |

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
- �� Dark mode support