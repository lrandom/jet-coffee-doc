# File Upload

> A flexible file upload component with drag and drop support, preview capabilities, and progress tracking.

## Basic Usage

```html
<script>
  import JCFileUpload from '@lib/Form/FileUpload/JCFileUpload.svelte';
  
  let files = [];
  
  function handleUpload(event) {
    const uploadedFiles = event.detail.files;
    // Handle uploaded files
  }
</script>

<!-- Basic usage -->
<JCFileUpload
  bind:files
  on:upload={handleUpload}
  accept="image/*"
/>
```

## Examples

### Drag and Drop

```html
<JCFileUpload
  dragDrop
  placeholder="Drag files here or click to upload"
/>
```

### With Preview

```html
<JCFileUpload
  showPreview
  maxFiles={5}
  accept="image/*"
/>
```

### With Progress

```html
<JCFileUpload
  showProgress
  multiple
  maxSize={5242880} <!-- 5MB -->
/>
```

### Custom Styling

```html
<JCFileUpload
  class="custom-upload"
  buttonText="Choose Files"
  dropzoneClass="custom-dropzone"
/>
```

## API

### Props

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `files` | `File[]` | [] | Array of selected files |
| `accept` | `string` | undefined | Accepted file types |
| `multiple` | `boolean` | false | Allow multiple file selection |
| `dragDrop` | `boolean` | false | Enable drag and drop |
| `maxFiles` | `number` | undefined | Maximum number of files |
| `maxSize` | `number` | undefined | Maximum file size in bytes |
| `showPreview` | `boolean` | false | Show file previews |
| `showProgress` | `boolean` | false | Show upload progress |
| `disabled` | `boolean` | false | Disable file upload |
| `buttonText` | `string` | 'Upload Files' | Custom button text |
| `placeholder` | `string` | 'Choose files or drag them here' | Custom placeholder text |

### Events

| Name | Description |
|------|-------------|
| `upload` | Fired when files are selected |
| `error` | Fired when an error occurs |
| `progress` | Fired during file upload |
| `remove` | Fired when a file is removed |

### Slots

| Name | Description |
|------|-------------|
| default | Custom upload button content |
| preview | Custom file preview template |
| placeholder | Custom placeholder content |
| progress | Custom progress indicator |

## Features

- 📁 Drag and drop support
- 🖼️ File preview
- 📊 Upload progress
- ⚡ Multiple file support
- 🔍 File type validation
- 📏 File size validation
- 🎨 Customizable appearance
- 🌙 Dark mode support

## Styling

### Default Styles

```css
/* Base upload styles */
.jc-upload {
  @apply relative border-2 border-dashed rounded-lg p-4;
  @apply border-gray-300 dark:border-gray-600;
}

/* Dropzone active state */
.jc-upload--active {
  @apply border-primary-500 bg-primary-50;
  @apply dark:border-primary-400 dark:bg-primary-900/10;
}

/* Preview container */
.jc-upload__preview {
  @apply grid grid-cols-4 gap-4 mt-4;
}

/* Preview item */
.jc-upload__preview-item {
  @apply relative rounded-lg overflow-hidden;
  @apply bg-gray-100 dark:bg-gray-800;
}

/* Progress bar */
.jc-upload__progress {
  @apply w-full h-2 bg-gray-200 rounded-full overflow-hidden;
  @apply dark:bg-gray-700;
}

/* Progress indicator */
.jc-upload__progress-bar {
  @apply h-full bg-primary-500 transition-all;
}
```

### Customization

You can customize the appearance using:
- Custom button and placeholder text
- Preview layout customization
- Progress bar styling
- Dark mode support
- Custom CSS classes
- Slot overrides

## Accessibility

The file upload component follows accessibility best practices:

- Keyboard navigation support
- Screen reader announcements
- ARIA attributes
- Focus management
- Error messaging
- Progress updates 