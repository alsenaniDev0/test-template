# Safhat Template Sample

This folder is a complete starter template for Safhat.

Files:

- `index.html`
- `style.css`
- `template.json`

Important rules:

1. Every normal visible block has:
   - a `show...` select field in `template.json`
   - a real field with `visibleWhen` and optional `requiredWhen`
   - a `sections` entry with the same `visibleWhen`
   - an HTML element with `data-section="sameKey"`

2. RSVP and feelings are platform features:
   - use `data-feature="rsvp"`
   - use `data-feature="feelings"`
   - control them from the app feature checkboxes, not from normal dropdowns

3. Field font controls need a selector:

```json
"designControls": {
  "font": {
    "enabled": true,
    "label": "خط العنوان",
    "selector": ".title"
  }
}
```

4. Repeater fields render with:

```html
{{#each services}}
  <h3>{{title}}</h3>
{{/each}}
```

5. List fields render with:

```html
{{#each tags}}
  <span>{{this}}</span>
{{/each}}
```
