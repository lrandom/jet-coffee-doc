# File Upload

> A flexible file upload component with drag and drop support, preview capabilities, and progress tracking.

## Basic Usage

```html
<script>
  import { JCFileUpload } from '@lib/Form/FileUpload';
  
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


## Accessibility

The file upload component follows accessibility best practices:

- Keyboard navigation support
- Screen reader announcements
- ARIA attributes
- Focus management
- Error messaging
- Progress updates 