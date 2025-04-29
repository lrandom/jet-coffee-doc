# Slider

> A customizable slider component for selecting numeric values with support for range selection and custom steps.

## Basic Usage

```html
<script>
  import { JCSlider } from '@lib/Form/Slider';
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

## Styling

### Default Styles

```css
/* Base slider styles */
.jc-slider {
  @apply relative w-full h-2;
}

/* Track styles */
.jc-slider__track {
  @apply absolute h-2 rounded-full bg-gray-200;
  @apply dark:bg-gray-700;
}

/* Track fill */
.jc-slider__track-fill {
  @apply absolute h-full rounded-full bg-primary-500;
  @apply dark:bg-primary-400;
}

/* Thumb styles */
.jc-slider__thumb {
  @apply absolute w-4 h-4 rounded-full bg-white border-2;
  @apply border-primary-500 dark:border-primary-400;
  @apply focus:ring-2 focus:ring-primary-500;
  @apply -translate-x-1/2 top-1/2 -translate-y-1/2;
}

/* Tick marks */
.jc-slider__tick {
  @apply absolute w-1 h-1 rounded-full bg-gray-300;
  @apply dark:bg-gray-600;
  @apply -translate-x-1/2 top-full mt-1;
}

/* Mark labels */
.jc-slider__mark {
  @apply absolute text-xs text-gray-600;
  @apply dark:text-gray-400;
  @apply -translate-x-1/2 top-full mt-4;
}

/* Disabled state */
.jc-slider--disabled {
  @apply opacity-50 cursor-not-allowed;
}
```

### Customization

You can customize the appearance using:
- Different colors through the `color` prop
- Custom thumb and mark templates
- Label formatting
- Track and thumb styling
- Dark mode support
- Custom mark positions

## Accessibility

The slider component follows accessibility best practices:

- ARIA slider role
- Keyboard navigation
- Value announcements
- Range boundaries
- Step increments
- Focus management
- Screen reader support 