# my-app

A minimal, dependency-free static website prepared for deployment on Cloudflare Pages.

The page displays:

- Title: `Hello World!`
- Text: `I'm Chansik Yun`

## Project structure

```text
my-app/
├── index.html   # Page structure and visible content
├── styles.css   # Responsive visual design
└── README.md    # Project and deployment documentation
```

## Run locally

No package installation or build command is required. Open `index.html` in a browser to preview the page.

For a local web server, run the following from the `my-app` directory if Python is installed:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Change the content

1. Open `index.html`.
2. Edit the text inside `<h1 id="page-title">` to change the title.
3. Edit the paragraph directly below it to change the message.
4. Open `styles.css` to adjust colors, spacing, or typography. The CSS comments explain each section.

## Deploy with Cloudflare Pages after pushing to GitHub

This project is intentionally not connected to GitHub or Cloudflare Pages yet.

After creating and pushing a `my-app` repository:

1. In Cloudflare, open **Workers & Pages** and choose **Create application** → **Pages** → **Connect to Git**.
2. Select the GitHub repository.
3. In the build settings, leave **Build command** empty because this is a static site.
4. Set **Build output directory** to `my-app` when this folder is inside a larger repository. If `my-app` becomes the repository root, use `/` instead.
5. Set the production branch (normally `main`) and choose **Save and Deploy**.

Cloudflare Pages will then deploy the static files in the selected output directory and can automatically redeploy future pushes to the connected branch.

## Notes

- No dependencies, credentials, or environment variables are required.
- The project includes no JavaScript because the requested page is static; this keeps loading and maintenance simple.
