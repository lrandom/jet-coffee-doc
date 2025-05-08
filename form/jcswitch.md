# Switch

> A toggle switch component for boolean input with customizable styling and labels.

## Basic Usage

```html
<script>
  import JCSwitch from '@lib/Form/Switch/JCSwitch.svelte';
  let checked = false;
</script>

<!-- Basic usage -->
<JCSwitch bind:checked />
```

## Examples

### With Labels

```html
<JCSwitch>
  Enable notifications
</JCSwitch>
```

### Different Sizes

```html
<JCSwitch size="sm">Small switch</JCSwitch>
<JCSwitch size="base">Base switch</JCSwitch>
<JCSwitch size="lg">Large switch</JCSwitch>
```

### Custom Colors

```html
<JCSwitch color="success">Success switch</JCSwitch>
<JCSwitch color="warning">Warning switch</JCSwitch>
<JCSwitch color="danger">Danger switch</JCSwitch>
```

### With Icons

```html
<JCSwitch>
  <svelte:fragment slot="checked-icon">✓</svelte:fragment>
  <svelte:fragment slot="unchecked-icon">✗</svelte:fragment>
  Toggle with icons
</JCSwitch>
```

## API

### Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `checked` | `boolean` | false | Whether the switch is checked |
| `disabled` | `boolean` | false | Whether the switch is disabled |
| `size` | `string` | 'base' | Size of the switch ('sm', 'base', 'lg') |
| `color` | `string` | 'primary' | Color theme ('primary', 'success', 'warning', 'danger') |
| `name` | `string` | undefined | Name attribute for the input |
| `required` | `boolean` | false | Whether the switch is required |
| `value` | `any` | undefined | Value attribute for the input |

### Events

| Name | Description |
|------|-------------|
| `change` | Fired when switch state changes |
| `focus` | Fired when switch receives focus |
| `blur` | Fired when switch loses focus |

### Slots

| Name | Description |
|------|-------------|
| default | Label content |
| checked-icon | Icon for checked state |
| unchecked-icon | Icon for unchecked state |

## Features

- 🎨 Multiple color themes
- 📏 Different sizes
- 🔄 Smooth transitions
- 🖼️ Custom icons
- ⌨️ Keyboard support
- 🌙 Dark mode support
- ♿ Accessibility features
- 📱 Touch friendly


## Accessibility

The switch component follows accessibility best practices:

- Uses native `<input type="checkbox">` under the hood
- Proper ARIA switch role
- Keyboard navigation
- Focus management
- State announcements
- Touch target sizing
- High contrast support 