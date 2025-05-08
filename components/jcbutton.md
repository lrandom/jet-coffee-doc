# Button Component

The JCButton component is a versatile and customizable button implementation that supports various styles, sizes, and states.

## Basic Usage

```html
<script>
  import JCButton from '@lib/Element/Button/JCButton.svelte';
  
  // Svelte 5 state management
  let $isLoading = $state(false);
  let $buttonType = $state('primary');
  
  function handleClick() {
    $isLoading = true;
    setTimeout(() => $isLoading = false, 2000);
  }
</script>

<JCButton 
  label="Click Me"
  type={$buttonType}
  loading={$isLoading}
  on:click={handleClick}
/>
```

## Examples

### Different Types and Variants

```html
<script>
  import JCButton from '@lib/Element/Button/JCButton.svelte';
</script>

<JCButton type="primary" variant="solid" label="Primary Solid" />
<JCButton type="secondary" variant="soft" label="Secondary Soft" />
<JCButton type="danger" variant="outlined" label="Danger Outlined" />
<JCButton type="warning" variant="ghost" label="Warning Ghost" />
```

### Icon Button

```html
<script>
  import JCButton from '@lib/Element/Button/JCButton.svelte';
</script>

<JCButton iconButton type="primary">
					<svelte:fragment slot="icon">
						<i class="ti ti-map-pin-filled"></i>
					</svelte:fragment>
</JCButton>
```

### Link Button

```html
<script>
  import JCButton from '@lib/Element/Button/JCButton.svelte';
</script>

<JCButton 
  variant="link"
  to="/dashboard"
  label="Go to Dashboard"
/>
```

### Loading State

```html
<script>
  import JCButton from '@lib/Element/Button/JCButton.svelte';
  let $loading = $state(false);
  
  async function handleSubmit() {
    $loading = true;
    await submitForm();
    $loading = false;
  }
</script>

<JCButton 
  label="Submit"
  loading={$loading}
  on:click={handleSubmit}
/>
```

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

## Events

| Event | Description |
|-------|-------------|
| click | Fired when button is clicked |
| focus | Fired when button receives focus |
| blur | Fired when button loses focus |

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