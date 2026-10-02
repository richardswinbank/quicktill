# quicktill

A simple tap-to-add till for event bookstalls, designed for a phone.

- **Till** – one big button per item. Tap to add one to the current sale; the running total is at the bottom. Use the − on a button to take one off, **Clear** to abandon the sale, **Done** to record it and start the next.
- **Totals** – copies sold and takings per item for the event, with an undo for the last sale.
- **Setup** – add, rename, price, reorder and delete items.

Everything is stored on the phone itself (browser local storage). There is no server and no account, and it works offline once it has been opened once.

## Putting it on a phone

It is a static site with no build step, so it can be hosted anywhere that serves files over HTTPS. With GitHub Pages: repository **Settings → Pages → Deploy from a branch → main / root**, then open `https://<user>.github.io/quicktill/` on the phone and choose **Add to Home Screen**.

## Running locally

```bash
python -m http.server 8000
```

After changing any file, bump `CACHE` in `sw.js` so phones pick up the new version.
