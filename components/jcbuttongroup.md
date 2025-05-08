# JCButtonGroup

JCButtonGroup is a component that allows you to group multiple buttons together with consistent styling and spacing. It supports both horizontal and vertical orientations, with customizable spacing and sizing options.

## Features

- Horizontal or vertical button arrangement
- Configurable spacing between buttons
- Full-width support
- Consistent button sizing within the group
- Seamless connected appearance option
- Proper focus and hover states management

## Props

| Prop Name    | Type                           | Default       | Description                                      |
|--------------|--------------------------------|---------------|--------------------------------------------------|
| block        | boolean                        | false         | Makes the button group take full width           |
| space        | 'none' \| 'sm' \| 'md' \| 'lg' | 'none'       | Controls spacing between buttons                 |
| size         | 'xs' \| 'sm' \| 'base' \| 'lg' | 'base'       | Sets consistent size for all buttons in group    |

## Usage Examples

### Basic Usage

```svelte
<script>
import JCButton from '$lib/Element/Button/JCButton.svelte';
import JCButtonGroup from '$lib/Element/Button/JCButtonGroup.svelte';
</script>

<JCButtonGroup>
  <JCButton>Left</JCButton>
  <JCButton>Middle</JCButton>
  <JCButton>Right</JCButton>
</JCButtonGroup>
```

### With Spacing

```svelte
<JCButtonGroup space="md">
  <JCButton>First</JCButton>
  <JCButton>Second</JCButton>
  <JCButton>Third</JCButton>
</JCButtonGroup>
```

### Full Width

```svelte
<JCButtonGroup block>
  <JCButton>Left</JCButton>
  <JCButton>Middle</JCButton>
  <JCButton>Right</JCButton>
</JCButtonGroup>
```

### Custom Size

```svelte
<JCButtonGroup size="lg">
  <JCButton>Large</JCButton>
  <JCButton>Buttons</JCButton>
</JCButtonGroup>
```

## Styling

The component uses Tailwind CSS for styling and includes:

- Proper border radius handling for connected buttons
- Z-index management for hover states
- Responsive width handling
- Focus state management
- Dark mode support through Tailwind's dark mode classes

## Accessibility

- Maintains proper focus states for keyboard navigation
- Preserves button semantics and roles
- Ensures consistent spacing and sizing for better usability

## Best Practices

1. Use consistent button types within a group for visual harmony
2. Consider using the 'space' prop when buttons have different widths
3. Use the vertical orientation for stacked menu-like button groups
4. Apply the 'block' prop when you need the buttons to fill the container width

## Slots

The component accepts buttons as slot content:

```svelte
<JCButtonGroup>
  <slot />  <!-- Place JCButton components here -->
</JCButtonGroup>
```