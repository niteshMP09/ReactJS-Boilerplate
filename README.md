# React Boilerplate Project 🧱

This project is a **React + Vite** boilerplate setup with **ESLint**, **Prettier**, **Husky**, and **Dependabot** pre-configured for development workflow automation and code quality.

---

## 🚀 Features

- ⚡ **Vite** for fast React development
- 🧹 **ESLint** for code linting and style enforcement
- 🎨 **Prettier** for code formatting
- 🐶 **Husky** for Git hooks (pre-commit checks)
- 🤖 **Dependabot** for automatic dependency updates

---

## 🛠️ Setup Instructions

### 1. Install dependencies
```bash
npm install
```

### 2. Run the development server
```bash
npm run dev
```

---

## 🧹 ESLint Setup

ESLint is already configured in this project to help maintain clean and consistent code.

To manually check lint errors, run:
```bash
npm run lint
```

If errors appear on save, check your `.vscode/settings.json`:
```json
{
  "editor.defaultFormatter": null,
  "editor.formatOnSave": false
}
```

---

## 🎨 Prettier Setup

To ensure consistent formatting, Prettier is used alongside ESLint.

Prettier configuration file: `.prettierrc`  
Ignored files: `.prettierignore`

---

## 🐶 Husky Setup

Husky enforces linting before commits.

If Husky isn’t installed properly, reinstall it using:
```bash
pnpm dlx husky init
```
Then, ensure your pre-commit file contains:
```bash
#!/bin/sh
. "$(dirname -- "$0")/_/husky.sh"

npm run lint
```

You can test Husky by making a commit — it will automatically run ESLint.

---

## 🤖 Dependabot Setup

Dependabot keeps your dependencies up to date automatically.

Configuration file: `.github/dependabot.yml`
```yaml
version: 2
updates:
  - package-ecosystem: "npm"
    directory: "/"
    schedule:
      interval: "weekly"
    open-pull-requests-limit: 10
    commit-message:
      prefix: "chore(deps)"
    ignore:
      - dependency-name: "react"
      - dependency-name: "react-dom"
```

After pushing this to GitHub, go to:
**Settings → Code security and analysis → Enable Dependabot alerts**

---

## 🧑‍💻 Development

Start the dev server:
```bash
npm run dev
```

Build for production:
```bash
npm run build
```

Preview build locally:
```bash
npm run preview
```

---

## ✅ Commit Messages

Follow [Conventional Commits](https://www.conventionalcommits.org/) for clarity and automation.

Examples:
```
chore: setup ESLint and Prettier
chore: configure Husky for pre-commit linting
chore: add Dependabot for automatic dependency updates
```

---

## 📂 Folder Structure

```
react-boilerplate/
├── .husky/                 # Git hooks
├── .vscode/                # VSCode settings
├── public/                 # Static assets
├── src/                    # Source code
├── .eslintrc.json          # ESLint configuration
├── .prettierrc             # Prettier configuration
├── .prettierignore         # Files ignored by Prettier
├── .github/dependabot.yml  # Dependabot configuration
├── package.json
└── vite.config.ts
```

---

## 🧾 License

This project is open source and available under the [MIT License](LICENSE).

---

Made with ❤️ by Nitesh Sikarwar