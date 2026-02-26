# PL-400.

Client Script in Power Platform
context objects in model‑driven app JavaScript 
executionContext
    └── formContext
            ├── data
            │     └── process (Business Process Flow)
            ├── ui
            │     ├── tabs
            │     ├── sections
            │     └── controls
            ├── attributes (columns)
            └── controls (fields on the screen)

executionContext — the event container
This object represents the event that triggered your function (OnLoad, OnChange, OnSave).

What it gives you
Access to formContext

Information about the event source (which field changed)

Ability to stop the event (e.g., prevent save)

Ability to detect save mode (auto-save, manual save, etc.)

Example
javascript
function onChange(executionContext) {
    const formContext = executionContext.getFormContext();
}
You almost always use executionContext only to get formContext.
