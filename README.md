# GutCare — put it on a web address (5 minutes)

**Why:** opening the HTML file directly from your phone gives the page an empty
"origin". Browsers block every API call from that state, so Gemini, Sarvam, Groq
and the rest refuse — no matter how good your key is. On a real https address
the same key works.

## Option 1 — Netlify Drop (fastest, no account needed at first)
1. On a computer, open https://app.netlify.com/drop
2. Drag this whole folder onto the page.
3. You get a URL like https://gutcare-xyz.netlify.app — open it on your phone.
4. Chrome menu → "Add to Home screen".

## Option 2 — GitHub Pages (works from a phone browser)
1. Create a public repository, e.g. `gutcare`.
2. Upload `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`.
3. Settings → Pages → Source: "Deploy from a branch" → main → / (root) → Save.
4. After a minute: https://YOURNAME.github.io/gutcare/

## Option 3 — Cloudflare Pages
1. https://dash.cloudflare.com → Workers & Pages → Create → Pages → Upload assets.
2. Upload this folder, deploy, open the given URL.

## Then
- Open the URL, More → AI assistant, paste the key, tap **Test**.
- If it still fails, the message now tells you which cause it is:
  blocked before the provider / key rejected / model name wrong / quota.
- Use **Find models** to list the models your key can actually use and tap one.

## Your data
Everything is stored in the browser on your phone (localStorage).
Use More → Export backup before changing phones or clearing site data.
