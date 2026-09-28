# The Berkshires Spotlight

A small static website made with plain HTML and CSS. It has no build step, runtime dependencies, form service, or tracking scripts, so it can be hosted as a static site on Cloudflare Pages.

## Preview locally

1. Open a terminal in this folder.
2. Run `python3 -m http.server 8000`.
3. Open the site served on your local machine at port 8000.
4. Press `Ctrl+C` in the terminal to stop the local server.

You can also open `index.html` directly, but using the local server is closer to how the deployed site will be served.

## Add the sample postcard

The sample postcard image is stored at `images/sample-postcard.png` and displayed in the sample section. Replace that file with an updated Berkshire mailing image when the first one is produced. Other image files can go in the same folder; they need to be added to `index.html` before they appear on the site.

The official Facebook page could not be accessed for image selection, so no Facebook images are included. The site links to the official page.

## Deploy to Cloudflare Pages

This site is plain static files. No build command or output folder is needed.

For a Git-integrated Cloudflare Pages project, connect the `rybazome/berkshires-spotlight` repository, use `main` as the production branch, leave the build command blank, and set the build output directory to `.` (the repository root). No environment variables or framework preset are needed.

1. Put this folder in a GitHub repository.
2. In the Cloudflare dashboard, open **Workers & Pages** and create a Pages project connected to that repository.
3. Use the production branch (usually `main`). Leave the build command empty and set the build output directory to `.` (the repository root).
4. Deploy. Cloudflare Pages will provide a `*.pages.dev` preview address.
5. In the Pages project, open **Custom domains** and add `theberkshiresspotlight.com`. Follow Cloudflare's domain instructions, then also add `www.theberkshiresspotlight.com` if you want the `www` address available.

Cloudflare may update dashboard labels over time. See the [Cloudflare Pages static HTML guide](https://developers.cloudflare.com/pages/framework-guides/deploy-anything/) for current steps. The domain must be active on Cloudflare for Pages to configure it directly; otherwise follow the DNS records Cloudflare shows for the custom domain.

## Files

- `index.html` contains the page content and semantic structure.
- `styles.css` contains colors, layout, responsive rules, and typography.
- `images/` contains the logo, featured photo, and sample postcard.

Edit the HTML to update wording, phone numbers, prices, and coverage. Edit the CSS variables at the top of `styles.css` to adjust the colors.
