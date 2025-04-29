# Avatar Component

The JCAvatar component is used to display user avatars or profile pictures with various sizes and styles.

## Props

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| color | string | 'primary' | Background color when image not loaded ('primary', 'secondary', 'success', 'danger', 'warning', 'info', 'light', 'dark') |
| size | string | 'base' | Avatar size ('xs', 'sm', 'base', 'lg', 'xl') |
| src | string | 'img/avatar/avatar1.jpg' | Image source URL |
| rounded | boolean | true | Makes avatar fully rounded |
| placeholder | string | '' | Placeholder image URL while loading |

## Sizes

- **xs**: 24x24 pixels (w-6 h-6)
- **sm**: 32x32 pixels (w-8 h-8)
- **base**: 48x48 pixels (w-12 h-12)
- **lg**: 64x64 pixels (w-16 h-16)
- **xl**: 80x80 pixels (w-20 h-20)

## Features

- Lazy loading of images
- Loading placeholder/animation
- Custom color support
- Interactive (clickable)
- Supports all mouse and keyboard events

## Slots

- **default**: Custom content instead of image 