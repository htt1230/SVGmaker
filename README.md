# SVGmaker

Browser-based raster-to-SVG prototype. HEIC/HEIF, PNG, JPEG and WebP inputs are supported in the prototype. Image cropping, edge-connected light-background removal, and vector tracing happen in the browser.

## Run locally

Open `index.html` from a local web server (for example, `python -m http.server 8000`) and visit `http://localhost:8000`. The prototype loads ImageTracerJS and heic2any from jsDelivr. An internet connection is needed the first time those libraries are fetched.

## Publish with GitHub Pages

The workflow in `.github/workflows/pages.yml` deploys the `main` branch to GitHub Pages after a push. In the repository's **Settings → Pages**, select **GitHub Actions** as the build and deployment source if Pages has not been enabled yet. After the first successful deployment, the Pages URL is shown in the repository's Pages settings and the Actions run.

## Prototype notes

- Images are not uploaded by the app; tracing is performed in the browser.
- HEIC is converted to PNG locally using heic2any.
- Background removal only removes a selected near-white color connected to the image edges. It does not identify arbitrary objects or remove complex backgrounds.
- Use artwork, logos, or illustrations with relatively simple colors for cleaner tracing. Photographs are approximated as colored paths.
- This is an interaction prototype, not a production-ready image processing service.
