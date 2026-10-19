# Publishing the Holistic Life website

## Before you publish

1. Fill in every `[PLACEHOLDER]` in `impressum.html` and `datenschutz.html` (search for `PLACEHOLDER`).
2. In `index.html`, replace `holisticlife.at` with your real domain (4 lines near the top). This makes the LinkedIn preview image work.
3. Files to upload: `index.html`, `styles.css`, `impressum.html`, `datenschutz.html` and all `.png` files. Nothing else is needed.

## Option A: Netlify (easiest, no account on GitHub needed)

1. Go to https://app.netlify.com/drop and sign up for a free account.
2. Drag the folder with the website files onto the page. After a few seconds you get a link like `random-name.netlify.app`. Open it and check the site.
3. Site configuration > Change site name, if you want a nicer temporary address.
4. Domain management > Add a domain > enter your domain (e.g. `holisticlife.at`) > Verify > Add domain.
5. Netlify now shows the DNS records you need. Log in where you bought the domain (e.g. World4You, easyname, GoDaddy) and open the DNS settings:
   - For `holisticlife.at` (the root): an `A` record pointing to `75.2.60.5`
   - For `www`: a `CNAME` record pointing to `your-site-name.netlify.app`
   (Always use the values Netlify shows you, in case they change.)
   Alternative: use Netlify DNS and change the domain's nameservers to the four Netlify nameservers shown.
6. Wait for DNS to update (usually under an hour, at most 48 hours). Netlify then issues a free HTTPS certificate automatically. Check under Domain management > HTTPS.
7. To update the site later: Deploys > drag the updated folder onto the deploy area.
8. Hosting provider for the Datenschutz page: Netlify, Inc., 512 2nd Street, Suite 200, San Francisco, CA 94107, USA.

## Option B: GitHub Pages

1. Create a free account at https://github.com.
2. Click New repository, name it e.g. `holistic-life-website`, set it to Public, click Create.
3. Click "uploading an existing file", drag in all website files, then Commit changes.
4. Settings > Pages > Source: Deploy from a branch > Branch: `main`, folder `/ (root)` > Save. After a minute the site is live at `yourname.github.io/holistic-life-website`.
5. Settings > Pages > Custom domain: enter `holisticlife.at` > Save. (This creates a `CNAME` file in the repository; leave it there.)
6. At your domain registrar, add these DNS records:
   - Four `A` records for the root domain: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - A `CNAME` record for `www` pointing to `yourname.github.io`
7. Once DNS has updated, return to Settings > Pages and tick Enforce HTTPS.
8. Hosting provider for the Datenschutz page: GitHub, Inc., 88 Colin P. Kelly Jr. Street, San Francisco, CA 94107, USA.

## Check the LinkedIn preview

Paste your URL into https://www.linkedin.com/post-inspector/ to see the preview and refresh LinkedIn's cache after changes.
