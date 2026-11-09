# CS-02 Positive Form 10 Nomination

A one-page site. A cadet scans a QR code or NFC sticker, answers 4 questions, and their phone fills in an AFCW IMT 10. They then send it to the acting First Sergeant.

The PDF is built entirely on the phone. Nothing is stored or sent to a server.

## Files

| File | What it is |
|---|---|
| `index.html` | The nomination form |
| `form10-template.pdf` | Blank AFCW IMT 10, with all old example data removed |
| `qr.html` | Printable QR-code sign that points at the form |

## Change the First Sergeant

Open `index.html` and edit this line near the top:

```js
firstSergeantEmail: "c29satyam.shah@afacademy.af.edu"
```

Commit the change. The live site updates within a minute or two.

## Put it on GitHub Pages (about 5 minutes, free)

1. Sign in at github.com and create a **new public repository**, e.g. `cs02-form10`.
2. Click **Add file → Upload files**, drag in `index.html`, `form10-template.pdf`, and `qr.html`, then click **Commit changes**.
3. Go to **Settings → Pages**. Under "Build and deployment", set Source = **Deploy from a branch** and Branch = **main** / **(root)**, then click **Save**.
4. After about a minute the site is live at `https://<your-username>.github.io/cs02-form10/`.

The repository only holds the blank form and page code. Cadets' answers never go to GitHub.

## Make the sticker

- **QR:** open `https://<your-username>.github.io/cs02-form10/qr.html` and click **Print sign**.
- **NFC:** with a free app such as NXP TagWriter, write a **URL** record of `https://<your-username>.github.io/cs02-form10/` to the tag.

## How the form maps to the Form 10

| Question | Form 10 block |
|---|---|
| 1. Your rank and name | Blk 5 RO (Last, First, MI) + Blk 6 Grade; Blk 7 = CS-02 |
| 2. Nominee's rank and name | Blk 1 Cadet Name + Blk 3 Class Year (from cadet rank) ; Blk 2 = CS-02 |
| 3. What they did | Sec II Conduct Narrative |
| 4. Recommended reward | "Recommended Reward:" line in the narrative |
| (automatic) | Blk 4 Date = today; Blk 8 RO MFR = No |

Sections III–VII are left blank for the chain of command.
