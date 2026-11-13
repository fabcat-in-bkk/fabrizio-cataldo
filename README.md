# fabriziocataldo.com

Personal site. Static HTML, hand-written CSS, vanilla JS.
No framework, no build step, no dependencies.
Vercel Web Analytics only: cookieless, no personal data, no cross-site tracking.

    index.html      the whole site, self-contained
    cv/index.html   printable, ATS-readable CV; the single source for the CV
                    view on the home page, which loads it on demand
    og.png          social card, 1200x630
    vercel.json     clean URLs and security headers
    DEPLOY.md       how to deploy this

Fonts (Archivo variable, Instrument Sans, JetBrains Mono) are subset to the
glyphs the page uses and embedded as base64, as is the portrait. That is why the
page itself is a single HTTP request, plus one deferred analytics script and the
CV page, fetched once the browser is idle.

Both canvases do their own projection maths in a 2D context: an orthographic dot
globe with great-circle route arcs in the hero, and a cumulative capability chart
in the stack section. No WebGL, no charting library.

Copy is inline in the HTML on purpose so a crawler with no JavaScript sees every
word. The CV lives only in cv/index.html, which is a full page of its own. Search for the section comments to find what you want to edit.
