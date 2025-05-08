# Alert Component

The JCAlert component is a flexible alert/notification component that supports various styles and states.

## Basic Usage

```svelte
<script>
  import JCAlert from '$lib/Element/Alert/JCAlert.svelte';
</script>

<JCAlert type="success">
  This is a success alert
</JCAlert>
```

## Examples

### Different Alert Types

```svelte
<script>
  import JCAlert from '$lib/Element/Alert/JCAlert.svelte';
</script>

<JCAlert type="primary">Primary alert</JCAlert>
<JCAlert type="secondary">Secondary alert</JCAlert>
<JCAlert type="success">Success alert</JCAlert>
<JCAlert type="danger">Danger alert</JCAlert>
<JCAlert type="warning">Warning alert</JCAlert>
```

### Alert Variants

```svelte
<script>
  import JCAlert from '$lib/Element/Alert/JCAlert.svelte';
</script>

<JCAlert type="primary" variant="default">Default variant</JCAlert>
<JCAlert type="primary" variant="solid">Solid variant</JCAlert>
<JCAlert type="primary" variant="outline">Outline variant</JCAlert>
<JCAlert type="primary" variant="left-border">Left border variant</JCAlert>
<JCAlert type="primary" variant="top-border">Top border variant</JCAlert>
```

### Alert with Icon

```svelte
<script>
  import JCAlert from '$lib/Element/Alert/JCAlert.svelte';
</script>

<JCAlert type="info" labelIcon>
  <svelte:fragment slot="labelIcon">
    <div class="rounded-md p-2 flex items-center justify-between bg-info-600 text-white">
      <i class="ti ti-info-circle"></i>
    </div>
  </svelte:fragment>
  Alert with custom icon
</JCAlert>
```

### Closeable Alert

```svelte
<script>
  import JCAlert from '$lib/Element/Alert/JCAlert.svelte';
  
  function handleClose(event) {
    console.log('Alert closed', event.detail);
  }
</script>

<JCAlert type="warning" closeable on:onClose={handleClose}>
  Click the X button to close this alert
</JCAlert>
```

### Conditional Rendering

```svelte
<script>
  import JCAlert from '$lib/Element/Alert/JCAlert.svelte';
  
  let showAlert = true;
  
  function toggleAlert() {
    showAlert = !showAlert;
  }
</script>

<JCAlert type="success" show={showAlert}>
  This alert can be toggled
</JCAlert>

<button on:click={toggleAlert}>
  {showAlert ? 'Hide' : 'Show'} Alert
</button>
```

## Props

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| type | string | 'danger' | Alert type ('primary', 'secondary', 'danger', 'success', 'warning') |
| variant | string | 'default' | Alert style variant ('default', 'solid', 'outline', 'left-border', 'top-border') |
| labelIcon | boolean | false | Shows an icon label |
| closeable | boolean | false | Adds a close button |
| show | boolean | true | Controls alert visibility |

## Events

- **onClose**: Triggered when the alert is closed

## Slots

- **default**: Main content of the alert
- **labelIcon**: Custom icon content 

## Variants

- **default**: Light colored background with matching text
- **solid**: Filled background with white text
- **outline**: White background with colored border
- **left-border**: Left border with light background
- **top-border**: Top border with light background 