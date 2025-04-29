# Alert Component

The JCAlert component is a flexible alert/notification component that supports various styles and states.

## Props

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| type | string | 'danger' | Alert type ('primary', 'secondary', 'danger', 'success', 'warning') |
| variant | string | 'default' | Alert style variant ('default', 'solid', 'outline', 'left-border', 'top-border') |
| labelIcon | boolean | false | Shows an icon label |
| closeable | boolean | false | Adds a close button |
| show | boolean | true | Controls alert visibility |

## Variants

- **default**: Light colored background with matching text
- **solid**: Filled background with white text
- **outline**: White background with colored border
- **left-border**: Left border with light background
- **top-border**: Top border with light background

## Events

- **onClose**: Triggered when the alert is closed

## Slots

- **default**: Main content of the alert
- **labelIcon**: Custom icon content 