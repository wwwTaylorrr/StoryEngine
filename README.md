# StoryEngine project website

Static website for **StoryEngine: A State-Grounded Agentic Framework for Video Storytelling**.

## Files

- `index.html`: the website entry point.
- `styles.css` and `app.js`: layout and interaction.
- `site-data.js` and `assets/site-data.json`: matching copies of the page data.
- `assets/videos/`: five demonstrations and nine method-comparison videos.
- `assets/posters/`: video thumbnails and the social preview image.
- `assets/figures/`: four figures displayed on the page.
- `tools/check_site.py`: local link, asset, and benchmark checks.
- `.github/workflows/pages.yml`: an optional static GitHub Pages workflow.

## Preview

Open `index.html` in a browser. All page resources are stored locally and use relative paths. For HTTP video seeking, use a local server supporting byte-range requests. The website needs no backend, credentials, or npm installation.

## Page content

The sections are the project title, the manuscript's full abstract, Demonstrations, Comparisons, Overview Framework, Benchmark, and Citation. Demonstrations follow the instruments, cooperage, glasswork, locksmith, and net-making order. Comparisons follow the notebook, painter, and recipe order. The qualitative ablation figure (Fig. 3) follows Fig. 2 in the framework section.

The benchmark table reproduces the manuscript. Avg is the mean of seven video metrics, excluding PEC. Shared playback controls preserve the source clips' relative timing; shorter clips hold their final frame.

## Checks

```bash
python tools/check_site.py
node --check app.js
node --check site-data.js
```

## Deployment

The optional GitHub Actions workflow deploys this folder as a static Pages artifact when `main` changes. Configure the hosting destination for the repository that will contain the website.

Layout and interaction references: [SCOPE](https://z2tong.github.io/SCOPE/), [WorldMind](https://teawhite.cn/WorldMind/), and [StatePlay](https://jimntu.github.io/stateplay_page/). No reference-site media assets were imported.
