# Button Component

The JCButton component is a versatile and customizable button implementation that supports various styles, sizes, and states.

## Props

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| label | string | 'Button' | The text content of the button |
| type | string | 'primary' | Button type ('primary', 'secondary', 'danger', 'warning', 'success', 'info') |
| variant | string | 'solid' | Button variant ('solid', 'soft', 'outlined', 'link', 'ghost', 'gradient', 'elevated') |
| size | string \| number | 'base' | Button size ('lg', 'base', 'sm', 'xs' or number) |
| disabled | boolean | false | Whether the button is disabled |
| loading | boolean | false | Shows loading state |
| tag | string | 'button' | HTML element tag to use |
| block | boolean | false | Makes button full width |
| rounded | boolean | false | Makes button fully rounded |
| ring | boolean | true | Shows focus ring |
| iconButton | boolean | false | Makes button circular for icon use |
| formInputType | string | '' | HTML button type attribute |
| ripple | boolean | true | Enables ripple effect |
| elevation | boolean | false | Adds shadow elevation |
| iconOnly | boolean | false | Optimizes button for icon-only content |
| iconPosition | string | 'left' | Icon position ('left' or 'right') |
| to | string | '' | Navigation target for link buttons |

## Variants

- **solid**: Filled background with white text
- **soft**: Light colored background with matching text
- **outlined**: Transparent background with colored border
- **link**: Text-only appearance with hover effects
- **ghost**: Transparent background with colored text
- **gradient**: Gradient background effect
- **elevated**: White/dark background with shadow

## Sizes

- **lg**: Large size (h-12)
- **base**: Default size (h-10)
- **sm**: Small size (h-8)
- **xs**: Extra small size (h-6)
- **custom**: Can use number value for custom size in rem 