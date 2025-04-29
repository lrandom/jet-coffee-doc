# Select

> A customizable select component with support for single and multiple selection, search, and grouping.

## Basic Usage

```html
<script>
  import { JCSelect } from '@lib/Form/Select';
  
  let value = '';
  let options = [
    { value: 'option1', label: 'Option 1' },
    { value: 'option2', label: 'Option 2' },
    { value: 'option3', label: 'Option 3' }
  ];
</script>

<!-- Basic usage -->
<JCSelect
  bind:value
  {options}
  label="Select an option"
/>
```

## Examples

### Multiple Selection

```html
<script>
  let selectedValues = [];
</script>

<JCSelect
  multiple
  bind:value={selectedValues}
  options={options}
  placeholder="Select multiple options"
/>
```

### With Search

```html
<JCSelect
  searchable
  options={options}
  placeholder="Search and select"
/>
```

### Grouped Options

```html
<script>
  let groupedOptions = [
    {
      label: 'Group 1',
      options: [
        { value: '1.1', label: 'Option 1.1' },
        { value: '1.2', label: 'Option 1.2' }
      ]
    },
    {
      label: 'Group 2',
      options: [
        { value: '2.1', label: 'Option 2.1' },
        { value: '2.2', label: 'Option 2.2' }
      ]
    }
  ];
</script>

<JCSelect
  options={groupedOptions}
  placeholder="Select from groups"
/>
```

## API

### Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `value` | `any` | undefined | Selected value(s) |
| `options` | `Array` | [] | Array of options or option groups |
| `label` | `string` | undefined | Label text |
| `placeholder` | `string` | 'Select...' | Placeholder text |
| `multiple` | `boolean` | false | Enable multiple selection |
| `searchable` | `boolean` | false | Enable search functionality |
| `disabled` | `boolean` | false | Disable the select |
| `required` | `boolean` | false | Make the select required |
| `error` | `string` | undefined | Error message |
| `size` | `string` | 'base' | Select size ('sm', 'base', 'lg') |
| `clearable` | `boolean` | false | Show clear button |

### Events

| Name | Description |
|------|-------------|
| `change` | Fired when selection changes |
| `focus` | Fired when select receives focus |
| `blur` | Fired when select loses focus |
| `search` | Fired when search text changes |
| `clear` | Fired when selection is cleared |

### Slots

| Name | Description |
|------|-------------|
| option | Custom option template |
| selected | Custom selected value template |
| group | Custom group header template |
| no-results | Custom no results message |

## Features

- 📝 Single and multiple selection
- 🔍 Search functionality
- 👥 Option grouping
- 🎨 Customizable appearance
- ❌ Clearable selection
- ⌨️ Keyboard navigation
- 📱 Mobile friendly
- 🌙 Dark mode support

## Styling

### Default Styles

```css
/* Base select styles */
.jc-select {
  @apply relative w-full;
}

/* Select trigger */
.jc-select__trigger {
  @apply w-full rounded-md border border-gray-300;
  @apply bg-white dark:bg-gray-700;
  @apply focus:ring-2 focus:ring-primary-500;
}

/* Options container */
.jc-select__options {
  @apply absolute w-full mt-1 bg-white rounded-md shadow-lg;
  @apply dark:bg-gray-700 dark:border dark:border-gray-600;
  @apply max-h-60 overflow-auto z-50;
}

/* Option item */
.jc-select__option {
  @apply px-4 py-2 cursor-pointer;
  @apply hover:bg-gray-100 dark:hover:bg-gray-600;
}

/* Selected option */
.jc-select__option--selected {
  @apply bg-primary-50 text-primary-900;
  @apply dark:bg-primary-900/20 dark:text-primary-100;
}

/* Group header */
.jc-select__group-header {
  @apply px-4 py-2 text-sm font-medium text-gray-700;
  @apply dark:text-gray-300;
}

/* Search input */
.jc-select__search {
  @apply w-full px-4 py-2 border-b;
  @apply dark:bg-gray-700 dark:border-gray-600;
}
```

### Customization

You can customize the appearance using:
- Different sizes through the `size` prop
- Custom option templates
- Custom selected value display
- Group header styling
- Search input styling
- Dark mode support

## Accessibility

The select component follows accessibility best practices:

- ARIA combobox role
- Keyboard navigation
- Screen reader support
- Focus management
- Clear selection announcements
- Search functionality announcements 