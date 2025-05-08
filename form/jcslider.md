# Slider

> A customizable slider component for selecting numeric values with support for range selection and custom steps.

## Basic Usage

```html
<script>
  import JCSlider from '@lib/Form/Slider/JCSlider.svelte';
  let value = 50;
</script>

<!-- Basic usage -->
<JCSlider
  bind:value
  min={0}
  max={100}
  step={1}
/>
```

## Examples

### Range Slider

```html
<script>
  let range = [20, 80];
</script>

<JCSlider
  range
  bind:value={range}
  min={0}
  max={100}
/>
```

### With Labels

```html
<JCSlider
  value={50}
  showLabels
  labelFormatter={(v) => `${v}%`}
/>
```

### Custom Steps

```html
<JCSlider
  value={5}
  min={0}
  max={10}
  step={0.5}
  showTicks
/>
```

### With Marks

```html
<JCSlider
  value={50}
  marks={[
    { value: 0, label: 'Min' },
    { value: 50, label: 'Mid' },
    { value: 100, label: 'Max' }
  ]}
/>
```

## API

### Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `value` | `number \| number[]` | 0 | Current value or range values |
| `min` | `number` | 0 | Minimum value |
| `max` | `number` | 100 | Maximum value |
| `step` | `number` | 1 | Step increment |
| `range` | `boolean` | false | Enable range selection |
| `disabled` | `boolean` | false | Disable the slider |
| `showLabels` | `boolean` | false | Show min/max labels |
| `showTicks` | `boolean` | false | Show tick marks |
| `marks` | `Array` | [] | Custom marks on the slider |
| `labelFormatter` | `Function` | v => v | Format label text |
| `color` | `string` | 'primary' | Color theme of the slider |

### Events

| Name | Description |
|------|-------------|
| `change` | Fired when value changes |
| `input` | Fired during value changes |
| `dragstart` | Fired when dragging starts |
| `dragend` | Fired when dragging ends |

### Slots

| Name | Description |
|------|-------------|
| label | Custom label template |
| thumb | Custom thumb template |
| mark | Custom mark template |

## Features

- 📊 Single and range values
- 📏 Custom step sizes
- 🎯 Custom marks
- 🏷️ Formatted labels
- ⚡ Smooth animations
- 🎨 Customizable appearance
- ⌨️ Keyboard support
- 🌙 Dark mode support


## Accessibility

The slider component follows accessibility best practices:

- ARIA slider role
- Keyboard navigation
- Value announcements
- Range boundaries
- Step increments
- Focus management
- Screen reader support 