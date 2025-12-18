# Next.js Boilerplate

A production-ready foundation for building modern web applications with Next.js, React, and TypeScript.

<p>
  <a href="https://nextjs.org/"><img src="https://img.shields.io/badge/Next.js-16.0.9-black?style=flat-square&logo=next.js&logoColor=white" alt="Next.js" /></a>
  <a href="https://react.dev/"><img src="https://img.shields.io/badge/React-19.2.3-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React" /></a>
  <a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TypeScript-5.9.3-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" /></a>
  <a href="https://tailwindcss.com/"><img src="https://img.shields.io/badge/Tailwind_CSS-4.1.18-06B6D4?style=flat-square&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" /></a>
  <a href="./LICENSE"><img src="https://img.shields.io/badge/License-MIT-green.svg?style=flat-square" alt="MIT License" /></a>
</p>

## Features

- **Next.js 16** with App Router and Turbopack for fast development
- **React 19** with experimental React Compiler support
- **TypeScript** with strict configuration
- **Tailwind CSS v4** for styling with dark/light theme support
- **Biome** for linting and formatting (fast alternative to ESLint + Prettier)
- **Husky + lint-staged** for pre-commit code quality checks
- **Renovate** for automated dependency updates
- **Security headers** pre-configured (CSP, HSTS, X-Frame-Options, etc.)

---

## Quick Start

### Prerequisites

- Node.js 22 or later
- pnpm (recommended), npm, or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/sujalxplores/next-js-boilerplate.git
cd next-js-boilerplate

# Install dependencies
pnpm install

# Start the development server
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## Scripts

| Command | Description |
|---------|-------------|
| `pnpm dev` | Start development server with Turbopack |
| `pnpm build` | Create production build |
| `pnpm start` | Start production server |
| `pnpm lint` | Check code with Biome |
| `pnpm lint:fix` | Fix linting issues with Biome |

---

## Project Structure

```
next-js-boilerplate/
├── app/
│   ├── components/           # React components
│   │   └── ThemeToggle.tsx
│   ├── favicon.ico
│   ├── globals.css           # Global styles and Tailwind
│   ├── layout.tsx            # Root layout
│   └── page.tsx              # Home page
├── public/                   # Static assets
├── .husky/                   # Git hooks
├── biome.json                # Biome config
├── next.config.ts            # Next.js config
├── postcss.config.mjs        # PostCSS config
└── tsconfig.json             # TypeScript config
```

---

## Tech Stack

| Category | Technology | Version |
|----------|------------|---------|
| Framework | [Next.js](https://nextjs.org/) | 16.0.9 |
| UI | [React](https://react.dev/) | 19.2.3 |
| Language | [TypeScript](https://www.typescriptlang.org/) | 5.9.3 |
| Styling | [Tailwind CSS](https://tailwindcss.com/) | 4.1.18 |
| Theming | [next-themes](https://github.com/pacocoursey/next-themes) | 0.4.6 |
| Linting | [Biome](https://biomejs.dev/) | 2.3.10 |
| Git Hooks | [Husky](https://typicode.github.io/husky/) | 9.1.7 |

---

## Configuration

### TypeScript

Strict mode is enabled with additional checks:

```json
{
  "compilerOptions": {
    "strict": true,
    "noUnusedLocals": true,
    "noUnusedParameters": true
  }
}
```

### Biome

Configured for consistent code style. Runs automatically on pre-commit via Husky.

### Security Headers

Pre-configured in `next.config.ts`:

- Content-Security-Policy
- X-Frame-Options
- X-Content-Type-Options
- Referrer-Policy
- Permissions-Policy

---

## Theming

Dark and light mode support using `next-themes`. The `ThemeToggle` component is included for switching themes.

```tsx
<ThemeProvider attribute="class" defaultTheme="system">
  <App />
</ThemeProvider>
```

---

## Deployment

### Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/sujalxplores/next-js-boilerplate)

```bash
pnpm build
vercel
```

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

```bash
# Fork and clone
git clone https://github.com/your-username/next-js-boilerplate.git

# Create a branch
git checkout -b feature/your-feature

# Make changes and commit (Husky will run pre-commit hooks)
git commit -m "feat: add new feature"

# Push and open a PR
git push origin feature/your-feature
```

---

## License

MIT - see [LICENSE](LICENSE) for details.

---

## Resources

- [Next.js Documentation](https://nextjs.org/docs)
- [Tailwind CSS Docs](https://tailwindcss.com/docs)
- [Biome Docs](https://biomejs.dev/guides/getting-started/)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
