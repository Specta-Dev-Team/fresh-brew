# Fresh Brew Design System

A consistent, modern UI template system for all Fresh Brew application screens.

## 📁 Structure

```
template/
├── css/
│   ├── design-system.css    # Core variables, colors, typography
│   └── components.css        # Reusable UI components
├── snippets/
│   └── components.html       # Copy-paste HTML snippets
├── template-base.html        # Full page template
└── design-guide.html         # Visual component guide
```

## 🎨 Design Tokens

### Colors
- **Primary**: `#4F46E5` (Indigo)
- **Primary Hover**: `#4338CA`
- **Secondary**: `#64748B` (Slate)
- **Background**: `#F3F4F6`
- **Text**: `#111827`

### Typography
- **Font Family**: Inter (Google Fonts)
- **Icons**: Material Icons

### Spacing
- **Small**: 0.5rem
- **Medium**: 1rem
- **Large**: 1.5rem

## 🚀 Quick Start

### 1. Include CSS Files
```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
<link rel="stylesheet" href="../template/css/design-system.css">
<link rel="stylesheet" href="../template/css/components.css">
```

### 2. Use the Wrapper
```html
<div class="fb-wrapper">
    <div class="fb-glass-card">
        <!-- Your content -->
    </div>
</div>
```

## 📦 Components

### Buttons
```html
<!-- Primary Button -->
<button class="fb-btn fb-btn-primary">
    <span class="material-icons">check</span>
    Submit
</button>

<!-- Secondary Button -->
<button class="fb-btn fb-btn-secondary">
    <span class="material-icons">add</span>
    New
</button>

<!-- White Button -->
<button class="fb-btn fb-btn-white">Cancel</button>

<!-- Small Button -->
<button class="fb-btn fb-btn-primary fb-btn-sm">Small</button>
```

### Form Fields
```html
<div class="fb-form-group">
    <label class="required">Field Name</label>
    <input type="text" placeholder="Enter value">
</div>

<!-- Dropdown -->
<div class="fb-form-group">
    <label>Select Field</label>
    <select>
        <option value="">Select an option</option>
    </select>
</div>

<!-- Toggle Switch -->
<div class="fb-form-group">
    <label>Enable Feature</label>
    <label class="fb-toggle-switch">
        <input type="checkbox">
        <span class="fb-toggle-slider"></span>
    </label>
</div>
```

### Grid Layouts
```html
<!-- 2 Columns -->
<div class="fb-grid-2">
    <div class="fb-form-group">...</div>
    <div class="fb-form-group">...</div>
</div>

<!-- 3 Columns -->
<div class="fb-grid-3">...</div>

<!-- 4 Columns -->
<div class="fb-grid-4">...</div>

<!-- 6 Columns -->
<div class="fb-grid-6">...</div>
```

### Tables
```html
<div class="fb-table-container">
    <table class="fb-table">
        <thead>
            <tr>
                <th>Column 1</th>
                <th>Column 2</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><input type="text"></td>
                <td><input type="text"></td>
            </tr>
        </tbody>
    </table>
</div>
```

### Tabs
```html
<div class="fb-tabs">
    <button class="fb-tab active" onclick="activateTab(0)">Tab 1</button>
    <button class="fb-tab" onclick="activateTab(1)">Tab 2</button>
</div>

<div id="tab0" class="fb-tab-content active">Content 1</div>
<div id="tab1" class="fb-tab-content">Content 2</div>
```

### Side Panel
```html
<!-- Overlay -->
<div class="fb-panel-overlay" id="panelOverlay" onclick="togglePanel()"></div>

<!-- Panel -->
<div class="fb-panel" id="sidePanel">
    <div class="fb-panel-header">
        <h2>Panel Title</h2>
        <button class="fb-panel-close" onclick="togglePanel()">
            <span class="material-icons">close</span>
        </button>
    </div>
    <div class="fb-panel-content">
        <!-- Panel content -->
    </div>
</div>
```

## 🎯 Usage Guidelines

### Class Prefix
All classes use the `fb-` prefix (Fresh Brew) to avoid conflicts:
- `fb-btn` - Buttons
- `fb-form-group` - Form groups
- `fb-table` - Tables
- `fb-grid-*` - Grid layouts

### Responsive Design
- Grids automatically stack on mobile devices
- Side panels become full-width on tablets/mobile
- Tables have horizontal scroll on small screens

### Icons
Use Material Icons for consistency:
```html
<span class="material-icons">icon_name</span>
```

Common icons:
- `add` - Add/New actions
- `check` - Submit/Confirm
- `close` - Close/Cancel
- `edit` - Edit actions
- `delete` - Delete actions
- `search` - Search functionality
- `receipt_long` - Summary/Reports

## 🔧 Customization

### Modify Colors
Edit `design-system.css`:
```css
:root {
    --primary: #YOUR_COLOR;
    --primary-hover: #YOUR_HOVER_COLOR;
}
```

### Adjust Spacing
Edit spacing variables:
```css
:root {
    --font-size-base: 0.9rem;
    /* Adjust as needed */
}
```

## 📱 Responsive Breakpoints
- **Mobile**: < 640px
- **Tablet**: 640px - 1024px
- **Desktop**: > 1024px

## ✅ Best Practices

1. **Always use the wrapper**: Start with `fb-wrapper` and `fb-glass-card`
2. **Consistent spacing**: Use the grid classes for layouts
3. **Required fields**: Add `.required` class to labels
4. **Material Icons**: Use for all icons (consistency)
5. **Form validation**: Add visual feedback with border colors
6. **Button hierarchy**: Primary > Secondary > White

## 🆘 Common Patterns

### Page Header with Actions
```html
<div class="fb-header">
    <div class="fb-page-title">
        <h1>Page Title</h1>
    </div>
    <div class="fb-header-actions">
        <button class="fb-btn fb-btn-primary">Action</button>
    </div>
</div>
```

### Section with Title
```html
<div class="fb-section-title">
    <span class="material-icons">description</span>
    Section Name
</div>
<div class="fb-grid-4">
    <!-- Form fields -->
</div>
```

### Footer Actions
```html
<div class="fb-footer">
    <button class="fb-btn fb-btn-secondary">Cancel</button>
    <button class="fb-btn fb-btn-primary">Submit</button>
</div>
```

## 📄 License
Internal use for Fresh Brew application only.
