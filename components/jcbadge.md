# Badge Component

The JCBadge component is a versatile badge/indicator that can be used to show notifications, status, or counts.

## Props

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| content | string | '' | Text content of the badge |
| type | string | 'primary' | Badge type ('primary', 'secondary', 'success', 'danger', 'warning', 'info', 'light', 'dark') |
| rounded | boolean | true | Makes badge fully rounded |
| dot | boolean | false | Shows badge as a dot |
| icon | boolean | false | Enables icon slot |
| position | string | 'top-right' | Badge position ('top-right', 'top-left', 'bottom-right', 'bottom-left') |
| offsetX | number | dot ? 11 : 18 | Horizontal offset in pixels |
| offsetY | number | dot ? 11 : 18 | Vertical offset in pixels |
| border | boolean | false | Adds white border around badge |

## Slots

- **default**: Content that the badge will be attached to
- **icon**: Custom icon content when icon prop is true

## Styles

- Minimum size: 22x22 pixels (non-dot)
- Dot size: 10x10 pixels
- Font size: Extra small (xs)
- Font weight: Semi-bold 