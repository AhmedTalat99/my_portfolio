# GitHub Pages Deployment Configuration

This project is automatically deployed to GitHub Pages whenever you push to the `main` branch.

## Deployment Status

✅ **Automated Deployment Enabled**

Your Flutter web app will be automatically built and deployed to:
- **URL**: `https://AhmedTalat99.github.io/my_portfolio/`

## How it Works

1. Push code to the `main` branch
2. GitHub Actions workflow automatically triggers
3. Flutter builds the web version
4. The built app is deployed to GitHub Pages
5. Your portfolio is live within ~5-10 minutes

## GitHub Actions Workflow

The deployment workflow is defined in `.github/workflows/deploy.yml` and:
- Runs on every push to main
- Builds Flutter web with `--release` flag
- Uses `peaceiris/actions-gh-pages` for deployment
- Deploys to the `gh-pages` branch

## Local Development

```bash
# Get dependencies
flutter pub get

# Run in development mode
flutter run -d chrome

# Build for production (manual build)
flutter build web --release --base-href=/my_portfolio/
```