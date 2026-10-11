# IONOS blog integration

The marketing homepage is previewed on GitHub Pages. **The production blog stays on IONOS** because GitHub Pages cannot run PHP.

## Production layout
- `index.html`, `site.css`, `logo.svg`: app-first marketing homepage
- `blog.php`, `blog-posts.json`, `blog-api.php`: blog and public interactions
- `business/index.html`, `business/blog-manager-api.php`: protected editor and comment moderation
- `blog-config.php` and `business/blog-manager-config.php`: server-only, NEVER commit

## Deployment checklist
1. Back up the current IONOS webroot, database, and live `blog-posts.json`.
2. Compare live posts with the six-post staging snapshot to avoid overwriting newer content.
3. Protect the editor with IONOS HTTP authentication; keep real config files outside public GitHub.
4. Deploy to a PHP-capable staging subdomain, not GitHub Pages.
5. Verify posts, editor login, draft/publish, comment approval, likes, consent and legal pages.
6. Confirm the privacy notice covers comment handling, then deploy the approved site to derdiedasdie.de.

The original trainers remain archived and unlinked. **No automatic production deployment is configured.**
