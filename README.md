# Invoice Dashboard

Welcome to **Invoice Dashboard**, a Next.js application that allows you to create, delete, and manage invoices through a clean, modern interface. You can also view insights and statistics such as how many invoices have been created, giving you a clear overview of your billing activity.

This README provides an overview of the project's dependencies and functionality, and explains how to get it running using **pnpm**.

---

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Dependencies](#dependencies)  
   - [Production Dependencies](#production-dependencies)  
   - [Development Dependencies](#development-dependencies)  
3. [Getting Started](#getting-started)  
   - [Installation](#installation)  
   - [Scripts](#scripts)  
4. [Contributing](#contributing)  
5. [License](#license)

---

## Project Overview

**Invoice Dashboard** is built with:

- **Next.js** (15.0.4-canary.33) for rendering an interactive dashboard with server-side rendering and client-side transitions  
- **React** (19.0.0-rc) and **React DOM** (19.0.0-rc) for the latest React features and efficient UI updates  
- **NextAuth** (5.0.0-beta.25) for handling user authentication flows  
- **Tailwind CSS** (3.4.4) and **@tailwindcss/forms** for styling and form utilities  
- **Heroicons** for easily adding beautiful SVG icons  
- **@vercel/postgres** (0.8.0) to store, update, and query invoices quickly (especially suited for deployments on Vercel)  
- **Zod** for schema validation of invoice data and user input  
- **TypeScript** for type-safe development  
- **bcrypt** for secure password hashing

With these tools, you can manage invoices—creating, updating, and deleting them—and view essential metrics like the total number of invoices, enabling you to monitor your invoicing activity effectively.

---

## Dependencies

### Production Dependencies

| Package                   | Version                         | Purpose                                                                                              |
| ------------------------- | ------------------------------- | ---------------------------------------------------------------------------------------------------- |
| **[@heroicons/react]**   | ^2.1.4                         | Beautiful, free MIT-licensed SVG icons by Tailwind Labs in React component form                      |
| **[@tailwindcss/forms]** | ^0.5.7                         | Tailwind CSS plugin providing a basic reset for form elements                                       |
| **[@vercel/postgres]**   | ^0.8.0                         | Simplified database handling via Vercel Postgres                                                     |
| **[autoprefixer]**       | 10.4.19                        | Parses CSS and adds vendor prefixes automatically                                                    |
| **[bcrypt]**             | ^5.1.1                         | A library to hash and compare passwords securely                                                     |
| **[clsx]**               | ^2.1.1                         | A utility for dynamically constructing `className` strings                                           |
| **[next]**               | 15.0.4-canary.33               | The Next.js React framework for server rendering and static site generation                          |
| **[next-auth]**          | 5.0.0-beta.25                  | Authentication for Next.js applications via OAuth, Email, or custom providers                        |
| **[postcss]**            | 8.4.38                         | A tool for transforming CSS with JavaScript                                                          |
| **[react]**              | 19.0.0-rc-cd22717c-20241013     | Latest release candidate of React                                                                    |
| **[react-dom]**          | 19.0.0-rc-cd22717c-20241013     | DOM-specific methods for React, aligning with the experimental React version                         |
| **[tailwindcss]**        | 3.4.4                          | Utility-first CSS framework                                                                          |
| **[typescript]**         | 5.5.2                          | A superset of JavaScript that adds static typing                                                     |
| **[use-debounce]**       | ^10.0.1                        | A simple hook for debouncing values or functions                                                     |
| **[zod]**                | ^3.23.8                        | TypeScript-first schema validation library                                                           |

### Development Dependencies

| Package                  | Version              | Purpose                                                                  |
| ------------------------ | -------------------- | ------------------------------------------------------------------------ |
| **[@types/bcrypt]**     | ^5.0.2               | TypeScript definitions for bcrypt                                        |
| **[@types/node]**       | 20.14.8              | TypeScript definitions for Node.js                                       |
| **[@types/react]**      | 19.0.0-rc.1          | TypeScript definitions for React                                         |
| **[@types/react-dom]**  | 19.0.0-rc.1          | TypeScript definitions for React DOM                                    |
| **[eslint]**            | ^9                   | A pluggable linter for JavaScript and JSX                               |
| **[eslint-config-next]**| 15.1.2               | Official ESLint configuration for Next.js                                |

### pnpm Overrides

Because we are using experimental versions of React and React DOM, we explicitly override the matching `@types/react` and `@types/react-dom`:

```json
"pnpm": {
  "overrides": {
    "@types/react": "npm:types-react@19.0.0-rc.1",
    "@types/react-dom": "npm:types-react-dom@19.0.0-rc.1"
  }
}
```

---

## Getting Started

### Installation

1. **Clone or download the repository**:
   ```bash
   git clone https://github.com/your-username/invoice-dashboard.git
   cd invoice-dashboard
   ```

2. **Install dependencies** using [pnpm](https://pnpm.io/):
   ```bash
   pnpm install
   ```

### Scripts

The available scripts in **package.json** are:

- **`pnpm run build`**  
  Builds the Next.js application for production.

- **`pnpm run dev`**  
  Runs the Next.js development server with the `--turbo` flag for experimental faster refresh.  
  Access the application at [http://localhost:3000](http://localhost:3000).

- **`pnpm run start`**  
  Runs the compiled application in production mode, typically after running `pnpm run build`.

- **`pnpm run lint`**  
  Lints your codebase using ESLint according to the Next.js configuration.

---

## Contributing

We welcome contributions! Whether you’re fixing a bug, proposing a new feature, or improving documentation:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/new-feature`.
3. Make your changes and commit them.
4. Push to your fork: `git push origin feature/new-feature`.
5. Open a Pull Request against the main branch.

---

## License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute this software as long as the original license is retained.

---

**Happy Invoicing!** If you have any questions or issues, feel free to open an issue or start a discussion. Enjoy managing your invoices with **Invoice Dashboard**!
