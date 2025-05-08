# Accordion Component

The JCAccordion component provides collapsible content sections for organizing information.

## Basic Usage

```svelte
<script>
  import JCAccordion from '$lib/Element/Accordion/JCAccordion.svelte';
  import JCAccordionItem from '$lib/Element/Accordion/JCAccordionItem.svelte';
</script>

<JCAccordion multiple={false}>
  <JCAccordionItem open={true}>
    <svelte:fragment slot="header">
      Section 1
    </svelte:fragment>
    <p>Content for section 1</p>
  </JCAccordionItem>
  
  <JCAccordionItem>
    <svelte:fragment slot="header">
      Section 2
    </svelte:fragment>
    <p>Content for section 2</p>
  </JCAccordionItem>
</JCAccordion>
```

## Props

### JCAccordion
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| multiple | boolean | false | Allow multiple sections to be open simultaneously |

### JCAccordionItem
| Prop | Type | Default | Description |
|------|------|---------|-------------|
| headerLabel | string | 'Accordion Item' | Label for the accordion header |
| open | boolean | false | Initial open state |

## Slots

### JCAccordion
- **default**: Container for accordion items

### JCAccordionItem
- **header**: Custom header content
- **default**: Content to be shown/hidden

## Features

- Smooth animations for expanding/collapsing
- Support for single or multiple open sections
- Customizable header content
- Ripple effect on header click
- Dark mode support 