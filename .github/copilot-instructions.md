# Test Automation Practice Site - AI Coding Guide

## Project Purpose
This is a web automation testing practice site with HTML pages designed to teach and test various web automation scenarios including locators, actions, synchronization, alerts, and form interactions.

## Architecture Overview

### Directory Structure
- **`examples/`** - Demo pages showcasing specific automation concepts (locators, actions, alerts, etc.)
- **`tasks/`** - Interactive exercises for practicing automation scenarios
- **`css/`** - Styling with W3.CSS framework + custom styles for test elements
- **`js/scripts.js`** - Central JavaScript file with all interactive behaviors
- **`menu.html`** - Shared navigation loaded via jQuery into each page

### Core Patterns

#### Page Structure Convention
All pages follow this template:
```html
<div id="header"></div> <!-- Loads menu.html via jQuery -->
<!-- Page content with test elements -->
```

#### CSS Class/ID Naming for Testing
- **Functional IDs**: `#start_green`, `#fb_name`, `#text` - Direct element identification
- **Container IDs**: `#green_loader`, `#test1`, `#standartText` - Group related elements
- **Test-specific classes**: `.text`, `.test`, `.vfb-desc` - Multiple element selection

#### JavaScript Architecture
Central `scripts.js` contains:
- **Timer-based functions**: `magic()`, `prepare_blue()` - For synchronization testing
- **Form validation**: `validateAge()`, `numberValidation()` - Input handling scenarios
- **Alert handlers**: `alertSummoning()`, `conformationOrDenial()` - Dialog interactions
- **Dynamic content**: Loading animations with `setTimeout()` patterns

## Key Development Patterns

### Adding New Test Pages
1. Copy existing page template from `examples/` or `tasks/`
2. Include standard CSS/JS links: `../css/style.css`, `../css/w3.css`, `../js/scripts.js`
3. Add `<div id="header"></div>` for navigation
4. Use descriptive IDs/classes for automation targeting

### Navigation Menu Updates
Modify `menu.html` dropdown sections:
- **Page Examples** dropdown: `#base_menu` container
- **Tasks** dropdown: `#sync_menu` container
- URLs follow pattern: `/example-site/examples/` or `/example-site/tasks/`

### JavaScript Function Patterns
- **Async operations**: Use `setTimeout()` for delays and loading states
- **Element manipulation**: jQuery for DOM updates, vanilla JS for direct access
- **Validation functions**: Return status via DOM updates, not console output

### CSS Styling Approach
- **W3.CSS framework**: Primary UI components (buttons, forms, layouts)
- **Custom styles**: Test-specific element highlighting and interactions
- **Button patterns**: Colored buttons with specific IDs (`#start_green`, `#start_green_and_blue`)

## Testing Scenarios Covered

### Element Location (`examples/locators.html`)
- Multiple elements with same class
- Nested div structures
- Mixed ID/class combinations

### User Actions (`examples/actions.html`) 
- Text input, checkboxes, radio buttons
- Date pickers, dropdowns
- Click and form submission

### Synchronization (`examples/sync.html`, `loading_color.html`)
- Timed color changes
- Sequential loading animations
- Element visibility toggles

### Alerts & Popups (`examples/alerts_popups.html`)
- Standard alerts, confirms, prompts
- Page navigation confirmations

### Form Workflows (`tasks/provide_feedback.html`, `enter_a_new_person.html`)
- Multi-step forms with validation
- Dynamic form field generation
- Error message handling

## Common Customizations
- **Add loading scenarios**: Extend timer patterns in `scripts.js`
- **New form validations**: Follow `validateAge()` function structure  
- **Additional locator patterns**: Use mixed class/ID combinations like existing examples
- **Menu expansion**: Add entries to appropriate dropdown in `menu.html`