# YAMA · Ergün Özsoy

The home base for the **YAMA** suite — a single landing page that links to every
app. Spaceship console concept, a hitchhiker's hub. Don't panic.

Trilingual (TR / DE / EN), single static file, no dependencies.

## Deploy as your platform root

To make this your main page at **`ergunozsoy.github.io`**:

1. Create a repository named exactly `ergunozsoy.github.io`.
2. Put this `index.html` in the root.
3. Settings → Pages → deploy from branch → `main` / root.

It will be live at `https://ergunozsoy.github.io/` and act as the front door to
all the other repos.

## Edit your modules

Everything lives in one array near the top of the `<script>` — `MODULES`.
Each entry:

```js
{ slug:"YAMA-Violin",      // exact GitHub repo name (case-sensitive)
  deck:"music",            // lang | music | finance | tools
  call:"VLN",              // 2–3 letter callsign on the card
  status:"online",         // online | beta  (sets the status light)
  web:true,                // true → shows a "Launch" button (GitHub Pages)
  desc:{ tr:"…", de:"…", en:"…" } }
```

Links are built automatically:
- **Launch** → `https://ergunozsoy.github.io/<slug>/` (only if `web:true`)
- **Code** → `https://github.com/ergunozsoy/<slug>`

If a web app doesn't have GitHub Pages enabled yet, either enable it
(Settings → Pages) or set `web:false` so only the Code button shows.

To add a new app: copy one line, change the fields. To regroup: change `deck`.
To add a whole new deck: add an id to `DECKS` and a label in each language's
`decks` block.

## Easter eggs

- **The towel** in the airlock — click it for Towel Day (May 25). On May 25 it
  greets you on its own.
- **42** in the footer — the Answer.
- **crew / Besatzung / mürettebat** in the footer — the honorary-passenger
  manifest, with a quiet bow to Oğuz Atay through Hikmet Benol.
- **DON'T PANIC** button, top right.

## Credits

Affectionate nods to Douglas Adams (*The Hitchhiker's Guide to the Galaxy*) and
to Oğuz Atay. Part of the **YAMA Project** · © 2026 Ergün Özsoy.

*Simple by design. Powerful by evolution.*
