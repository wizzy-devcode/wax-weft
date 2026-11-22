# Wax & Weft — print your own Ankara

This is a print-studio concept where anyone can design their own Ankara fabric.
It's one self-contained HTML file with no frameworks, no build step and no images: the patterns are drawn live with SVG. The only outside resource is Google Fonts.

## What you can do

- **Design a print.** Choose from four motifs (Sunburst, Palm fan, Diamond, River), four colourways (Lagos Noon, Indigo Market, Palm Wine, Hibiscus) and three scales (Small, Medium, Bold).
- **Watch it update instantly.** The fabric preview, the patterned strip under the header, the motif thumbnails and the hanging label all redraw as you choose.
- **Shuffle.** Can't decide? Hit **Shuffle** for a random combination.

## The inspiration

- **Subject:** Ankara wax-print fabric and how it's bought: often in six-yard lengths, then taken to a tailor.
- **Look:** details lifted from real cloth, such as the printed selvedge text along the top edge, the zig-zag pinked cut at the bottom and a hanging label tag. They sit on a loud, saturated palette with tilted highlight blocks behind the headline.
- **Interaction:** a product configurator. JavaScript builds the pattern from small SVG tiles. Neighbouring tiles swap colours or rotate, so the fabric reads as woven rather than stamped.
- **Trends it uses:** dopamine design (bright, saturated colour) and personalised product builders.

| Role | Colour |
| --- | --- |
| Yellow | `#ffd23f` |
| Pink | `#ff4f8b` |
| Cobalt | `#2340b5` |
| Ink | `#1a1530` |
| Cream | `#fff8ef` |

**Typefaces:** Syne for headings and Figtree for text, both from Google Fonts.

### Trend references
- Figma, [Top web design trends for 2026](https://www.figma.com/resource-library/web-design-trends/) (bright, saturated "dopamine" palettes)
- DesignRush, [Web Design Trends for 2026](https://www.designrush.com/agency/website-design-development/trends/web-design-trends) (expressive styles such as dopamine design)

## Files

```
wax-and-weft/
├── index.html   the whole page: HTML, CSS and JavaScript
└── README.md    this file
```

## Put it online with GitHub Pages

1. **Create a repository.** On GitHub, click **New repository**, name it `wax-and-weft`, set it to **Public**, and create it.
2. **Upload the files.** Choose **Add file → Upload files**, add `index.html` and `README.md`, then click **Commit changes**.
3. **Turn on Pages.** Go to **Settings → Pages** (under "Code and automation").
4. **Choose the source.** Under **Build and deployment → Source**, pick **Deploy from a branch**. Select `main` and `/ (root)`, then click **Save**.
5. **Open your site.** After a minute or two it will be live at `https://<your-username>.github.io/wax-and-weft/`.

GitHub Pages is free for public repositories.

> **Command line instead?**
> ```bash
> git init
> git add .
> git commit -m "Add Wax & Weft page"
> git branch -M main
> git remote add origin https://github.com/<your-username>/wax-and-weft.git
> git push -u origin main
> ```
> Then do steps 3–5 above.

> **Keeping several pages in one repository?** Upload this whole `wax-and-weft` folder to the top level of that repo instead.
> The page will then live at `https://<your-username>.github.io/<repo-name>/wax-and-weft/`.

## Make it yours

- **Fill in the placeholders.** `[PRICE]`, `[FABRIC]` and `[TURNAROUND]` are waiting for real information. Search the file for `[` to find them.
- **Add a colourway.** Add an entry to the `PALETTES` list near the bottom of the file (a ground colour plus three print colours). Then copy one of the colourway buttons and give it the next `data-i` number.
- **Add a motif.** Draw it inside the `motifSVG()` function on a 100 × 100 tile, add it to the `MOTIFS` list, and add a matching button.
- **The "Order 6 yards" button** is a placeholder. Point it at your own checkout, order form or WhatsApp link.

## Built to be friendly

- The page works on phones, tablets and desktops.
- Every choice is a real button with a pressed state, and the fabric preview has a text description that updates with each change.
- If someone has "reduce motion" turned on, transitions are switched off.
