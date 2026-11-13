# Ashutosh Ojha: personal website

A single-page static site. No build step, no framework: everything lives in `index.html`.

```
index.html                         the whole site (HTML, CSS, and the search-tree script)
Ashutosh_Ojha_CV.pdf               linked from the nav and the hero
photo.jpg                          portrait shown next to your name
papers/trace-answer-compatibility.pdf
.nojekyll                          tells GitHub Pages to serve files as-is
```

## Publish on GitHub Pages (about 5 minutes)

1. On GitHub, use the free organization **ashutoshoj** and its **public** repository named exactly `ashutoshoj.github.io`. The repository is `ashutoshoj/ashutoshoj.github.io`, owned through your existing personal account.
2. Open the repo, choose **Add file → Upload files**, and drag in everything from this folder, including the `papers` folder and `.nojekyll`. Commit.
3. Go to **Settings → Pages**. Under "Build and deployment", set Source to **Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
4. After a minute or two the site is live at `https://ashutoshoj.github.io`.

### Optional: your own domain

A domain like `ashutoshojha.com` reads better than a username on applications. After buying one:

1. In **Settings → Pages → Custom domain**, enter the domain and save. GitHub adds a `CNAME` file to the repo.
2. At your domain registrar, add four `A` records for the bare domain pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153` and `185.199.111.153`, plus a `CNAME` record for `www` pointing to `ashutoshoj.github.io`.
3. Once DNS has propagated, tick **Enforce HTTPS**.

## Editing

All content is plain HTML in `index.html`. Search for the section you want (`id="news"`, `id="publications"`, `id="experience"`, `id="honours"`).

- **Add a news item:** copy one `<li class="row">…</li>` block in News, paste it at the top, and change the date and text. Keep `datetime="YYYY-MM"` in sync with the visible date.
- **Add a paper:** copy a paper block in Publications. For a second paper in the same year, write the year as `<span class="sr">2026</span>` so it's hidden visually (the year shows once per group) but still read by screen readers.
- **Change the photo:** replace `photo.jpg` with another square image (640×640 works well). It's shown as a circle, so keep your face centered.
- **Update the CV:** replace `Ashutosh_Ojha_CV.pdf` with a new file of the same name.
- **Footer:** bump "Last updated" when you change things.

The page uses Gentium Book Plus from Google Fonts (the same family as your CV). It follows the visitor's light or dark setting automatically, and the search tree in the header is redrawn on every visit. Visitors who turn off motion get a static tree.

## Before you publish

- Your CV PDF is out of date with the site: it still says "EMNLP'26" (the paper is in Findings), "Under Review @ NeurIPS'26" for MEMENTO, an older title for the LensPINN paper, and it doesn't list the DiffuLM paper or the GSoC 2026 mentor role.
- The DiffuLM accepted-papers page still shows the older title ("…Mediates Prediction…"). You may want to ask the organizers to update it.
- JEE line: about 1 million candidates is the JEE Main pool; JEE Advanced has far fewer test-takers. Consider rewording that honour.
- The Kaggle "9th place" comes from the solution write-up on your Kaggle profile. Confirm it matches the final leaderboard.
- If you have a Google Scholar or OpenReview profile, add it to the links row (`class="links"`) and the footer.
