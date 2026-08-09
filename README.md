# fabriziocataldo.com

Personal site. Static HTML, hand-written CSS, vanilla JS.
No framework, no build step, no dependencies.
Vercel Web Analytics only: cookieless, no personal data, no cross-site tracking.

    index.html      the whole site, self-contained
    cv/index.html   printable, ATS-readable CV
    og.png          social card, 1200x630
    vercel.json     clean URLs and security headers
    DEPLOY.md       how to deploy this

Fonts (Archivo variable, Instrument Sans, JetBrains Mono) are subset to the
glyphs the page uses and embedded as base64, as is the portrait. That is why the
page itself is a single HTTP request, plus one deferred analytics script.

Both canvases do their own projection maths in a 2D context: an orthographic dot
globe with great-circle route arcs in the hero, and a cumulative capability chart
in the stack section. No WebGL, no charting library.

Copy is inline in the HTML on purpose so a crawler with no JavaScript sees every
word. Search for the section comments to find what you want to edit.

## Confidentiality

Figures from the most recent role are stated relative or non-monetary by design.
Do not replace them with absolute values on this site.
