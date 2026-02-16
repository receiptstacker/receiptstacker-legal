# Deploy these HTML files to GitHub Pages with Cloudflare domain

1. Create/open public GitHub repo (recommended: receiptstacker-legal-site).
2. Copy all files from this folder into repo root:
   - index.html
   - privacy-policy.html
   - terms-and-conditions.html
   - support.html
3. Commit and push to main.
4. In GitHub repo Settings → Pages:
   - Source: Deploy from branch
   - Branch: main
   - Folder: / (root)
5. Set custom domain in GitHub Pages to:
   - legal.receiptstacker.com
6. In Cloudflare DNS (receiptstacker.com), add:
   - Type: CNAME
   - Name: legal
   - Target: YOUR_GITHUB_USERNAME.github.io
   - Proxy status: DNS only
7. Enable Enforce HTTPS in GitHub Pages after cert is issued.
8. Use these URLs in app stores:
   - https://legal.receiptstacker.com/privacy-policy.html
   - https://legal.receiptstacker.com/terms-and-conditions.html
   - https://legal.receiptstacker.com/support.html

Notes:
- Keep the Cloudflare CNAME as DNS only for reliable GitHub Pages SSL/verification.
- Update support email and effective dates in HTML files before publishing.
