# Select

> A customizable select component with support for single and multiple selection, search, and grouping.

## Basic Usage

```html
<script>
  import JCSelect from '@lib/Form/Select/JCSelect.svelte';
  
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
| `size` | `string` | 'base' | Select size ('sm', 'md', 'base', 'lg') |
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


## Accessibility

The select component follows accessibility best practices:

- ARIA combobox role
- Keyboard navigation
- Screen reader support
- Focus management
- Clear selection announcements
- Search functionality announcements 