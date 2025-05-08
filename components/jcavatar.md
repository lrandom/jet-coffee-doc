# Avatar Component

The JCAvatar component is used to display user avatars or profile pictures with various sizes and styles.

## Basic Usage

```svelte
<script>
  import JCAvatar from '$lib/Element/Avatar/JCAvatar.svelte';
</script>

<JCAvatar src="/images/profile.jpg" />
```

## Examples

### Avatar Sizes

```svelte
<script>
  	import JCAvatar from '$lib/Element/Avatar/JCAvatar.svelte';
</script>

<JCAvatar size="xs" />
<JCAvatar size="sm" />
<JCAvatar size="base" />
<JCAvatar size="lg" />
<JCAvatar size="xl" />
```

### Avatar Colors

```svelte
<script>
  	import JCAvatar from '$lib/Element/Avatar/JCAvatar.svelte';
</script>

<JCAvatar color="primary" />
<JCAvatar color="secondary" />
<JCAvatar color="success" />
<JCAvatar color="danger" />
<JCAvatar color="warning" />
<JCAvatar color="info" />
<JCAvatar color="light" />
<JCAvatar color="dark" />
<JCAvatar color="#ff5500" />
```

### Square Avatar

```svelte
<script>
  	import JCAvatar from '$lib/Element/Avatar/JCAvatar.svelte';
</script>

<JCAvatar rounded={false} />
```

### Custom Content

```svelte
<script>
  	import JCAvatar from '$lib/Element/Avatar/JCAvatar.svelte';
</script>

<JCAvatar>
  <span class="text-white font-bold">JC</span>
</JCAvatar>
```

### Avatar Group

```svelte
<script>
  import JCAvatar from '$lib/Element/Avatar/JCAvatar.svelte';
  import JCAvatarGroup from '$lib/Element/Avatar/JCAvatarGroup.svelte';
</script>

<JCAvatarGroup>
  <JCAvatar src="/images/user1.jpg" />
  <JCAvatar src="/images/user2.jpg" />
  <JCAvatar src="/images/user3.jpg" />
  <JCAvatar>
    <span class="text-white font-bold">+5</span>
  </JCAvatar>
</JCAvatarGroup>
```

The JCAvatarGroup component arranges avatars in an overlapping stack. It automatically:

- Creates a horizontal flex layout
- Adds a negative margin to overlap avatars
- Applies a white border around each avatar
- Adds a hover effect to bring an avatar to the front when hovered
- Adds a scale transition for better interactivity

```css
/* CSS styles applied to JCAvatarGroup (from app.css) */
.jc-avatar-group {
  @apply flex flex-row items-center flex-wrap;
}

.jc-avatar-group > *:not(:last-child) {
  margin-right: -0.8rem;
}

.jc-avatar-group > * {
  @apply border-2 border-gray-100 rounded-full
  cursor-pointer
  transition duration-300
  ease-in-out transform
  hover:scale-125 hover:z-10;
}
```

### Customized Avatar Group

```svelte
<script>
  import JCAvatar from '$lib/Element/Avatar/JCAvatar.svelte';
  import JCAvatarGroup from '$lib/Element/Avatar/JCAvatarGroup.svelte';
</script>

<JCAvatarGroup>
  <JCAvatar src="/images/user1.jpg" size="sm" class="border-2 border-white dark:border-gray-800" />
  <JCAvatar src="/images/user2.jpg" size="sm" class="border-2 border-white dark:border-gray-800" />
  <JCAvatar src="/images/user3.jpg" size="sm" class="border-2 border-white dark:border-gray-800" />
  <JCAvatar src="/images/user4.jpg" size="sm" class="border-2 border-white dark:border-gray-800" />
  <JCAvatar class="bg-gradient-to-r from-blue-500 to-indigo-600 text-white border-2 border-white dark:border-gray-800">
    <span class="font-bold">10+</span>
  </JCAvatar>
</JCAvatarGroup>
```

## Props

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| color | string | 'primary' | Background color when image not loaded ('primary', 'secondary', 'success', 'danger', 'warning', 'info', 'light', 'dark') |
| size | string | 'base' | Avatar size ('xs', 'sm', 'base', 'lg', 'xl') |
| src | string | 'img/avatar/avatar1.jpg' | Image source URL |
| rounded | boolean | true | Makes avatar fully rounded |
| placeholder | string | '' | Placeholder image URL while loading |

## Slots

- **default**: Custom content instead of image 

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