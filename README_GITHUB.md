MyNotes - GitHub Pages ready package
-------------------------------------

Contents:
- index.html           -> Main SPA (static) with login using users.json
- index_pdfjs.html     -> PDF.js viewer (uses CDN)
- users.json           -> Sample users (edit as needed)
- assets/              -> logo and favicon
- pdfs/                -> class9..class12 placeholders (replace with real PDFs)

How to deploy:
1. Create a new repository on GitHub (public).
2. Upload everything inside the 'site' folder to the repository root (do not nest inside another folder).
   - Files should be at repository root: index.html, users.json, assets/, pdfs/, index_pdfjs.html, README.md
3. In repo Settings -> Pages: set Source to branch 'main' and folder '/' (root).
4. Your site will be available at: https://<your-username>.github.io/<repo-name>/

Important notes:
- users.json is fetched with fetch('./users.json') and must be present at repo root or in same folder as index.html.
- GitHub Pages is static hosting — no server-side code (PHP/Node) will run. The login here is client-side and not secure.
- For a secure login, host a backend (Render, Heroku, Vercel functions) and point fetch() to that API.

Custom domain:
- In GitHub Pages settings add your custom domain (www.example.com)
- Update your domain DNS: create A records (185.199.108.153, 185.199.109.153, 185.199.110.153,185.199.111.153) and add CNAME for www to <your-username>.github.io
- Wait for DNS propagation.

That's it. Replace placeholder PDFs with your real PDFs and push to GitHub.
