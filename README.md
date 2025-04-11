

# Angular JSON Forms Project

This project demonstrates the integration of [JSON Forms](https://jsonforms.io/) with **Angular 15** and **Tailwind CSS** for rendering dynamic forms using JSON schemas. It also includes custom renderers for specific UI requirements.



Project Structure

```
src/
├── app/
│   ├── custom-renderers/        # Custom renderer components
│   ├── schemas/                 # JSON schema and UI schema files
│   ├── services/                # Utility and data services
│   └── app.component.ts        # Main entry component
├── assets/
└── styles.css                  # Tailwind CSS config
```

---

Setup Instructions

 Clone the repository

```bash
git clone https://github.com/your-username/angular-jsonforms-project.git
cd angular-jsonforms-project
```

Install dependencies

```bash
npm install
```
 Run the development server

```bash
ng serve
```

Navigate to `http://localhost:4200/` in your browser.

---

JSON Structure Explanation

The forms are rendered dynamically using two JSON files:

Schema (`schema.json`)

Defines the structure of the data (i.e., form fields and types).

```json
{
  "type": "object",
  "properties": {
    "name": { "type": "string" },
    "age": { "type": "integer" },
    "email": { "type": "string", "format": "email" }
  },
  "required": ["name", "email"]
}


UI Schema (`uischema.json`)

Describes the layout and visual configuration.

```json
{
  "type": "VerticalLayout",
  "elements": [
    { "type": "Control", "scope": "#/properties/name" },
    { "type": "Control", "scope": "#/properties/email" },
    { "type": "Control", "scope": "#/properties/age" }
  ]
}


 Assumptions Made

- All forms are rendered based on valid and complete JSON Schema and UI Schema.
- Forms are primarily single-page, vertically structured layouts.
- Tailwind CSS is used for styling instead of Angular Material or Bootstrap.
- Custom renderers are required only for specific components (e.g., date pickers, toggles).
- No backend integration is assumed; form data is handled only on the client-side.



 Tech Stack

- Angular 15
- JSON Forms
- Tailwind CSS
- TypeScript



 TODO

-  Add backend integration (optional)
-  Form validation and error styling
-  Export form data as JSON
- Expand UI schema support (Grid layout, Tabs)

