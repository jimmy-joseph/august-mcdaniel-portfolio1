# August McDaniel Portfolio

Standalone static portfolio for deployment from GitHub to Cloudflare. It uses
plain HTML and CSS and does not require a build step.

## Deploy with Cloudflare Pages and GitHub

1. Create a new empty GitHub repository.
2. Upload everything in this folder to the repository root and commit it.
3. In Cloudflare, open **Workers & Pages** and choose **Create application**.
4. Select **Pages**, then **Connect to Git** and choose the repository.
5. Use these build settings:
   - Framework preset: `None`
   - Build command: leave blank
   - Build output directory: `public`
6. Deploy. Future pushes to the selected GitHub branch deploy automatically.

## Connect gusmcdaniel.com

Open the Pages project in Cloudflare, choose **Custom domains**, select **Set up
a custom domain**, and enter `gusmcdaniel.com`. Repeat for
`www.gusmcdaniel.com` if you want both versions.

## Edit the website

- Main content: `public/index.html`
- Styling: `public/styles.css`
- Photos and resume: files inside `public/`

## Optional direct Workers deployment

The included `wrangler.jsonc` also lets you deploy the same static files as a
Cloudflare Worker with `npx wrangler deploy`.
