# Baby Smash Website

## Deployment

- Hosted on **Azure Static Web Apps**
- Auto-deploys on push to `main` via GitHub Actions

## Cache Busting

CSS cache-busting is automatic:
- `index.html` contains `styles.css?v=__CACHE_BUST__`
- The GitHub Actions workflow replaces `__CACHE_BUST__` with the git commit hash on deploy
- No manual version bumping needed

## Development

To run locally:
```bash
python3 -m http.server 8080
```

Note: When running locally, CSS will show `?v=__CACHE_BUST__` which is fine for development.
