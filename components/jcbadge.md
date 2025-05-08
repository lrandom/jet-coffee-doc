# Badge Component

The JCBadge component is a versatile badge/indicator that can be used to show notifications, status, or counts.

## Basic Usage

```svelte
<script>
  import JCBadge from '$lib/Element/Badge/JCBadge.svelte';
</script>

<JCBadge content="5">
  <button class="btn">Notifications</button>
</JCBadge>
```

## Examples

### Different Types

```svelte
<script>
  import JCBadge from '$lib/Element/Badge/JCBadge.svelte';
</script>

<div class="flex gap-4">
  <JCBadge content="Primary" type="primary">
    <div class="p-4 border rounded">Item</div>
  </JCBadge>
  
  <JCBadge content="Success" type="success">
    <div class="p-4 border rounded">Item</div>
  </JCBadge>
  
  <JCBadge content="Danger" type="danger">
    <div class="p-4 border rounded">Item</div>
  </JCBadge>
</div>
```

### Dot Badge

```svelte
<script>
  import JCBadge from '$lib/Element/Badge/JCBadge.svelte';
</script>

<JCBadge dot type="danger">
  <span class="text-lg">New messages</span>
</JCBadge>
```

### With Icon

```svelte
<script>
  import JCBadge from '$lib/Element/Badge/JCBadge.svelte';
</script>

<JCBadge icon type="warning" position="bottom-right">
  <button class="btn btn-primary">Settings</button>
  <svelte:fragment slot="icon">
    ⚠️
  </svelte:fragment>
</JCBadge>
```

### Custom Position and Offset

```svelte
<script>
  import JCBadge from '$lib/Element/Badge/JCBadge.svelte';
</script>

<JCBadge 
  content="99+" 
  type="info" 
  position="top-left" 
  offsetX={5} 
  offsetY={5}
  border
>
  <div class="w-20 h-20 bg-gray-200 flex items-center justify-center">
    Box
  </div>
</JCBadge>
```

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