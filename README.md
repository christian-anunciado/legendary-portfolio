# Legendary Portfolio Monorepo

This is a monorepo for a professional web portfolio using pnpm workspaces with the `app` folder as the workspace root.

## Tech Stack

- **Frontend**: Astro with React components and Tailwind CSS
- **Backend/CMS**: PayloadCMS running on Next.js

## Structure

```
legendary-portfolio/
├── app/                    # Workspace packages
│   ├── astro/              # Astro frontend (portfolio-client)
│   ├── payload/            # PayloadCMS backend (portfolio-admin)
├── package.json            # Root package.json
├── pnpm-workspace.yaml     # Workspace configuration
```

## Getting Started

1. Install dependencies:
```bash
pnpm install
```

2. Environment Setup:
   - Configure your environment variables in `app/payload/.env` (see .env.example)

3. Run development servers:

```bash
# Run both frontend and backend
pnpm dev

# Run only frontend (Astro)
pnpm dev:astro

# Run only backend (PayloadCMS)
pnpm dev:payload
```

4. Build for production:
```bash
# Build everything
pnpm build

# Build only frontend
pnpm build:astro

# Build only backend
pnpm build:payload
```

## Development Workflow

### Running commands on specific packages

```bash
# Run a command in a specific package
pnpm --filter <package-name> <command>

# Examples:
pnpm --filter portfolio-client dev  # Run Astro dev server
pnpm --filter portfolio-admin dev   # Run PayloadCMS dev server
```

### Adding dependencies

```bash
# Add a dependency to a package
pnpm --filter <package-name> add <dependency>

# Examples:
pnpm --filter portfolio-client add @astrojs/image
pnpm --filter portfolio-admin add @payloadcms/plugin-cloud
```

## Deployment

The frontend and backend can be deployed separately:

- **Frontend**: The Astro site can be deployed to static hosting platforms like Netlify, Vercel, or GitHub Pages
- **Backend**: The PayloadCMS admin can be deployed to a Node.js hosting platform like Vercel, Railway, or Render
