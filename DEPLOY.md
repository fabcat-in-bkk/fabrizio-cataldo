# How changes go live

The site deploys from GitHub. Vercel watches the repository: every push to `main`
updates fabriziocataldo.com, and every push to any other branch gets its own
preview URL. There is no build step and no CLI needed.

## Make a change safely

1. Start a branch from an up-to-date main:

       git checkout main
       git pull
       git checkout -b short-description-of-change

2. Edit the files. Open `index.html` in a browser to check the page. The CV view
   loads `/cv`, which only works when served, so check the CV on the preview URL.

3. Commit and push the branch:

       git add .
       git commit -m "What changed"
       git push -u origin short-description-of-change

   Vercel builds a preview within a minute. The link shows on the commit in
   GitHub and under Deployments in the Vercel dashboard. Production is untouched.

4. When the preview looks right, merge and push main:

       git checkout main
       git merge short-description-of-change
       git push

   Vercel deploys production automatically.

## Undo a bad deploy

Vercel dashboard, the `fabriziocataldo` project, Deployments: find the last good
production deployment, open the three-dot menu and choose Promote to Production.
That is instant. Then fix or `git revert` the change on main so the next push does
not bring it back.

## Files

    index.html      the site
    cv/index.html   the CV page, and the single source for the CV view on the site
    og.png          link preview image, 1200x630
    robots.txt, sitemap.xml
    vercel.json     clean URLs and security headers
    _planning/      local planning notes, gitignored, never published
