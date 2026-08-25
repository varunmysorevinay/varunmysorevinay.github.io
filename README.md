# varunmysorevinay-pixel.github.io

Source for my portfolio site: **https://varunmysorevinay-pixel.github.io**

Manufacturing engineering portfolio — case studies from Harsco Rail, SR Enterprises, and Dynatech Tools, plus the open-source engineering tools that implement the analyses behind them.

## Structure

```
index.html              Landing page: results, case studies, tools, experience
assets/style.css        Single stylesheet, light and dark
case-studies/
  line-rebuild.html         Remanufacturing line rebuild — 63% → 84%, $195K
  mixed-model-flow.html     Fixed-position → mixed-model flow — 30% lead time
  erp-material-flow.html    Infor LN master data — 75% fewer shortages
  defect-reduction.html     DMAIC quality program — 20% defect reduction
  aerospace-and-spm.html    Aerospace components and special-purpose machines
```

## Design notes

Static HTML and CSS. No build step, no framework, no JavaScript, no external requests — the whole site is two file types and loads instantly on a phone.

Colours are defined as custom properties on `:root` and redefined for `prefers-color-scheme: dark`, so the site follows the reader's system theme. Layout uses CSS grid with `auto-fit` and `minmax`, so it reflows from desktop to phone without breakpoint-by-breakpoint maintenance. Wide tables scroll inside their own container rather than forcing the page sideways. Motion is disabled under `prefers-reduced-motion`.

## Running locally

```bash
python -m http.server 8899
```

Then open `http://localhost:8899`. Open the files directly and relative paths still resolve, but a server matches how GitHub Pages actually serves them.

## Related repositories

| Repository | What it does |
|---|---|
| [line-balancing-toolkit](https://github.com/varunmysorevinay-pixel/line-balancing-toolkit) | Takt, RPW station assignment, balance efficiency, bottleneck |
| [oee-analyzer](https://github.com/varunmysorevinay-pixel/oee-analyzer) | OEE with loss attribution and downtime Pareto |
| [time-study-toolkit](https://github.com/varunmysorevinay-pixel/time-study-toolkit) | Standard times with rating, allowances, sample-size check |
| [capacity-planning-model](https://github.com/varunmysorevinay-pixel/capacity-planning-model) | Load vs. capacity and Kingman queueing lead time |

## A note on confidentiality

Case studies describe work performed for the employers named, at the level of method and outcome. No proprietary drawings, routings, cost data, or customer information appears here or in the linked repositories, and every sample dataset in those repositories is synthetic.

## Contact

**Varun Mysore Vinay** — Manufacturing Engineer, Columbia, SC
varunmysorevinay@gmail.com · [LinkedIn](https://www.linkedin.com/in/varunmysorevinay)
