# Radio

> A customizable radio button component for single selection from a group of options.

## Basic Usage

```html
<script>
  import JCRadio from '@lib/Form/Radio/JCRadio.svelte';
  let selected = 'option1';
</script>

<!-- Basic usage -->
<JCRadio
  bind:group={selected}
  value="option1"
>
  Option 1
</JCRadio>
<JCRadio
  bind:group={selected}
  value="option2"
>
  Option 2
</JCRadio>
```

## Examples

### Different Sizes

```html
<JCRadio size="sm">Small radio</JCRadio>
<JCRadio size="base">Base radio</JCRadio>
<JCRadio size="lg">Large radio</JCRadio>
```

### Radio Group

```html
<script>
  let selectedValue = 'apple';
  const options = [
    { value: 'apple', label: 'Apple' },
    { value: 'banana', label: 'Banana' },
    { value: 'orange', label: 'Orange' }
  ];
</script>

<JCRadio.Group
  bind:value={selectedValue}
  options={options}
  name="fruits"
/>
```

### Custom Styling

```html
<JCRadio class="custom-radio" color="success">
  Custom styled radio
</JCRadio>
```

### Disabled State

```html
<JCRadio disabled>Disabled option</JCRadio>
```

## API

### Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `value` | `any` | undefined | Radio button value |
| `group` | `any` | undefined | Selected value in the group |
| `name` | `string` | undefined | Name attribute for the input |
| `disabled` | `boolean` | false | Whether the radio is disabled |
| `size` | `string` | 'base' | Size of the radio ('sm', 'base', 'lg') |
| `color` | `string` | 'primary' | Color theme of the radio |
| `required` | `boolean` | false | Whether the radio is required |

### Events

| Name | Description |
|------|-------------|
| `change` | Fired when selection changes |
| `focus` | Fired when radio receives focus |
| `blur` | Fired when radio loses focus |

### Slots

| Name | Description |
|------|-------------|
| default | Label content |

## Features

- 🎯 Single selection
- 📏 Multiple sizes
- 🎨 Color themes
- 👥 Group functionality
- ⌨️ Keyboard navigation
- 🌙 Dark mode support
- ♿ Accessibility features
- 📱 Touch friendly


## Accessibility

The radio component follows accessibility best practices:

- Uses native `<input type="radio">` element
- Proper grouping with fieldset and legend
- Keyboard navigation
- Focus management
- State announcements
- Touch target sizing
- High contrast support 