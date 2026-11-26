# Putting the gallery online

This folder (`_site`) is a complete website. Nothing needs installing or
building — it just needs somewhere to live. Two free options, both about
two minutes.

## Option 1 — Netlify Drop (fastest, no account needed to start)

1. Go to **https://app.netlify.com/drop**
2. Drag this whole `_site` folder onto the page.
3. It uploads and gives you a link straight away, something like
   `https://cheerful-marzipan-1a2b3c.netlify.app`.
4. Make a free account when it offers, or the site disappears after a while.
   With an account you can rename it to something like
   `isaiah-and-gilitza.netlify.app`.

## Option 2 — Cloudflare Pages

1. Go to **https://dash.cloudflare.com** → Workers & Pages → Create → Pages →
   Upload assets.
2. Name it, drag the `_site` folder, deploy.
3. You get `your-name.pages.dev`.

Either way the link is public: anyone you send it to can open it, on any
phone or computer, with no account and no app.

## What people can do there

- Look through the whole day in order, by the time each photo was taken
- Open anything full screen, zoom in, swipe between shots
- Watch the films, with sound
- Mark favourites (saved on their own device)
- **Download** any single photo, or the whole day in one file

## Sizes

- The photographs on the site are 1400px on the long edge — right for
  phones, laptops and ordinary prints, about 120KB each.
- `isaiah-and-gilitza.zip` is every photo and film in one download (113MB).
- The untouched originals (about 12-25MB each, 6.2GB in total) are **not**
  on the site. They stay in the wedding folder on your Mac. Anyone who wants
  one for a large print should ask you, and the gallery tells them so.

## If you add more photos later

In the wedding folder, run:

    bash _gallery/rebuild/rebuild.sh

That regenerates everything, including this site folder. Then rebuild the
archive and re-upload:

    cd _site && rm -f isaiah-and-gilitza.zip && zip -q -r -0 isaiah-and-gilitza.zip w v
