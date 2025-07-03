# blog
Innovation & Improvement Articles

## GitHub Actions Deployment

This repository includes a GitHub Actions workflow for automatic deployment to Cloudflare Pages.

### Setup Instructions

1. **Configure Repository Secrets**: Add the following secrets to your repository settings:
   - `CLOUDFLARE_API_TOKEN`: Your Cloudflare API token with Pages:Edit permissions
   - `CLOUDFLARE_ACCOUNT_ID`: Your Cloudflare account ID
   - `CLOUDFLARE_PROJECT_NAME`: Your Cloudflare Pages project name (optional, defaults to 'blog')

2. **Nuxt.js Configuration**: Ensure your project has:
   - `package.json` with dependencies and a `generate` script
   - Nuxt.js configuration for static site generation
   - Project source files in the appropriate directory structure

### Workflow Features

- **Automatic Deployment**: Triggers on every push to any branch
- **Node.js Environment**: Uses Node.js 20 LTS with npm dependency caching
- **Build Process**: Runs `npm run generate` to build the static site
- **Error Handling**: Gracefully handles missing configurations
- **Cloudflare Integration**: Deploys to Cloudflare Pages using the official wrangler action

The workflow file is located at `.github/workflows/nuxtjs.yml`.
