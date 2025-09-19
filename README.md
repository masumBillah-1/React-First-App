# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.


## APIs Used

These are the Programming Hero APIs this project interacts with:

| Endpoint               | Purpose                                                              |
| ---------------------- | -------------------------------------------------------------------- |
| `/api/all`             | Fetches data on **all countries**.                                   |
| `/api/alpha/{code}`    | Fetches data about a country by its **ISO alpha-code** (e.g. `116`). |
| `/api/lang/{language}` | Fetches countries where the specified **language** is spoken.        |
| `/api/name/{name}`     | Fetches data on a country (or countries) by its **common name**.     |



|Masum BIllah | Fetches data on **all countries**.  |

---

```js
// Fetch all countries
fetch("https://openapi.programming-hero.com/api/all")
  .then((res) => res.json())
  .then((data) => console.log(data));

// Fetch country by ISO code
fetch("https://openapi.programming-hero.com/api/alpha/116")
  .then((res) => res.json())
  .then((data) => console.log(data));

// Fetch countries by language
fetch("https://openapi.programming-hero.com/api/lang/english")
  .then((res) => res.json())
  .then((data) => console.log(data));

// Fetch country by name
fetch("https://openapi.programming-hero.com/api/name/bangladesh")
  .then((res) => res.json())
  .then((data) => console.log(data));
```