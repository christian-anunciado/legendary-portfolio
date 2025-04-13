# Legendary Portfolio Monorepo
### *Because one repo wasn't legendary enough*

This is a monorepo for my legendary and professional web portfolio. It's built with Astro, PayloadCMS, and Tailwind CSS.

## Tech Stack 🤓

- **Frontend**: Astro with React components and Tailwind CSS (it's literally rocket science 🚀)
- **Backend/CMS**: PayloadCMS running on Next.js (delivering your content faster than pizza delivery)

## Structure
### *AKA "Where did I put that file again?"*

```
legendary-portfolio/
├── app/                    # Where the magic happens
│   ├── astro/              # Astro frontend (portfolio-client) - your public face
│   ├── payload/            # PayloadCMS backend (portfolio-admin) - your secret lair
├── package.json            # The file everyone edits but nobody reads
├── pnpm-workspace.yaml     # Workspace configuration (dragons be here)
```

## Getting Started
### *Coffee recommended, patience required*

1. Install dependencies:
```bash
pnpm install # Now go make a sandwich while this runs
```

2. Environment Setup:
   - Configure your environment variables in `app/payload/.env` (see .env.example)
   - Pro tip: "PASSWORD123" is not a secure password, no matter how many times you've used it

3. Run development servers:

```bash
# Run both frontend and backend (for overachievers)
pnpm dev

# Run only frontend (Astro) - for when your backend is being temperamental
pnpm dev:astro

# Run only backend (PayloadCMS) - for when you just need to update content
pnpm dev:payload
```

4. Build for production:
```bash
# Build everything (and pray nothing breaks)
pnpm build

# Build only frontend (when the backend is someone else's problem)
pnpm build:astro

# Build only backend (when the frontend is someone else's problem)
pnpm build:payload
```

## Development Workflow
### *Or "How to look busy while actually accomplishing things"*

### Running commands on specific packages

```bash
# Run a command in a specific package
pnpm --filter <package-name> <command>

# Examples:
pnpm --filter portfolio-client dev  # Run Astro dev server (space mode activated)
pnpm --filter portfolio-admin dev   # Run PayloadCMS dev server (content wrangling mode)
```

### Adding dependencies
### *AKA "Making your node_modules folder even more massive"*

```bash
# Add a dependency to a package
pnpm --filter <package-name> add <dependency>

# Examples:
pnpm --filter portfolio-client add @astrojs/image  # For when your images need to look stellar
pnpm --filter portfolio-admin add @payloadcms/plugin-cloud  # For when your content needs to float
```

## Deployment
### *Launching your creation into the wild*

The frontend and backend can be deployed separately (they need their space):

- **Frontend**: The Astro site can be deployed to static hosting platforms like Netlify, Vercel, or GitHub Pages. It's like sending your child to college - emotional but necessary.
- **Backend**: The PayloadCMS admin can be deployed to a Node.js hosting platform like Vercel, Railway, or Render. It's the engine room - nobody sees it, but everyone notices when it breaks.

## Troubleshooting
### *When everything goes sideways*

- **Have you tried turning it off and on again?** No, seriously, restart your dev server.
- **Package not found errors?** That's just npm's way of saying "I don't know where I put that."
- **CSS looks weird?** Welcome to frontend development! Where everything works until it doesn't.
- **Can't remember a command?** That's what this README is for. We won't judge you for scrolling back up.

## Final Words of Wisdom

Remember, in the world of web development, there are only two hard problems: cache invalidation, naming things, and off-by-one errors.

Happy coding! May your builds be successful and your coffee be strong. 💻☕
