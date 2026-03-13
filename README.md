# UniWebsite

A personal CV / portfolio website for **Alex Spinks**, built as a single-page static HTML site.

## Features

- Responsive two-column CV layout with a fixed sidebar
- Accessibility controls: high-contrast toggle and adjustable font size
- Hover image effect and a collapsible "Show Additional Details" button
- Contact enquiry form with client-side validation
- No external build tools or frameworks required – pure HTML, CSS and JavaScript

## Project Structure

```
UniWebsite/
├── Index.html        # The entire single-page website
├── .do/
│   └── app.yaml      # Digital Ocean App Platform deployment spec
└── README.md
```

## Deploying to Digital Ocean App Platform

### Option 1 – Deploy button (one click)

[![Deploy to DO](https://www.deploytodo.com/do-btn-blue.svg)](https://cloud.digitalocean.com/apps/new?repo=https://github.com/AlexSpinks/UniWebsite/tree/main)

### Option 2 – Using the App Spec file

1. Install and authenticate the [Digital Ocean CLI (`doctl`)](https://docs.digitalocean.com/reference/doctl/how-to/install/).
2. Run the following command from the repository root:

   ```bash
   doctl apps create --spec .do/app.yaml
   ```

3. Digital Ocean will build and serve the static site. Any subsequent push to the `main` branch will trigger an automatic re-deploy.

### Option 3 – Digital Ocean Control Panel

1. Log in to [cloud.digitalocean.com](https://cloud.digitalocean.com).
2. Go to **Apps → Create App**.
3. Connect your GitHub account and select the **AlexSpinks/UniWebsite** repository.
4. Choose the `main` branch and confirm that Digital Ocean detects it as a **Static Site**.
5. Set **Index document** to `Index.html`.
6. Click **Next** through the remaining steps and then **Create Resources**.

The site will be available at the URL Digital Ocean assigns (e.g. `https://uniwebsite-xxxxx.ondigitalocean.app`).

## Running Locally

No build step is needed. Simply open `Index.html` in a browser:

```bash
# macOS
open Index.html

# Linux
xdg-open Index.html

# Windows (PowerShell)
Start-Process Index.html
```

Or use any static file server, for example:

```bash
npx serve .
# then visit http://localhost:3000
```

## License

© 2026 Alex Spinks. All rights reserved.
