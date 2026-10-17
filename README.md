# Seven Summits | Interactive Leaflet Map

**Created:** October 17, 2026  
**Assignment:** R Markdown webpage with a dated, interactive Leaflet map.

## Files

- `index.html` — ready-to-host interactive Leaflet webpage. This is the page GitHub Pages will display.
- `seven_summits.Rmd` — original R Markdown project, using the R `leaflet` package and the same mountain data. You can knit this separately with RStudio.
- `summits.json` — coordinates and descriptive data used for the HTML version.
- `.nojekyll` — tells GitHub Pages to publish the HTML as supplied.

## Publish with GitHub Pages

1. Sign in at https://github.com and create a **public** repository named `seven-summits-leaflet`.
2. Upload `index.html`, `seven_summits.Rmd`, `summits.json`, and `.nojekyll` into the **repository root**. Commit to the `main` branch.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**. Choose `main`, `/ (root)`, then **Save**.
5. Your public site should appear at `https://YOUR_USERNAME.github.io/seven-summits-leaflet/` (replace `YOUR_USERNAME` with your username). Use that actual published URL for your assignment.

## Knit the R Markdown source

Install R, RStudio and these packages once:

```r
install.packages(c("rmarkdown", "leaflet", "htmltools", "magrittr"))
```

Then in RStudio click **Knit** on `seven_summits.Rmd`, or run:

```r
rmarkdown::render("seven_summits.Rmd", output_file = "seven_summits_rendered.html")
```

The HTML site and the R Markdown source are intentionally two compatible outputs using the same theme and points. `index.html` is a standalone Leaflet.js implementation that can go directly to GitHub Pages without knitting. The `.Rmd` uses the R `leaflet` package for the academic source.

## Rubric checklist

- [x] Creation date visible: **October 17, 2026**.
- [x] Interactive Leaflet world map with seven clickable markers and map controls.
- [ ] Public hosting link: complete GitHub Pages publishing above.

## Internet requirement

For the online HTML map, Leaflet's JavaScript/CSS and CARTO/Esri base map tiles load from public web services. The R Markdown HTML widget also requires online tiles (though its JavaScript dependencies can be embedded by knitting with `self_contained: true`). Opening `index.html` without internet will show an informative fallback rather than an empty screen.
