# FC Barcelona UCL 2018-19: Away Fragility and the Anfield Collapse

A data analysis project examining why Barcelona, sitting on a 3-0 lead from the first leg, were beaten 4-0 at Anfield and eliminated from the Champions League.

The central question: was this a surprise, or were the warning signs already in the data?

---

## What's in this repo

```
barca_ucl_2019/
├── index.html              # The main report (open this in a browser)
├── data/                   # All source CSV files
├── figures/                # Static charts generated from the notebook
├── notebooks/
│   ├── barca_ucl_2019_analysis.ipynb   # Full analysis notebook (executed)
│   └── analysis.ipynb                  # Original exploratory notebook
└── README.md
```

---

## The report

Open `index.html` in any browser. No setup needed.

It covers:

- **Context**: the season's emotional backdrop, the Roma trauma from 2017-18, Iniesta's departure, the public pressure to win the trophy
- **Campaign overview**: all 12 matches with an interactive timeline
- **The core paradox**: Barcelona averaged higher possession away from home yet scored 56% fewer goals
- **Away fragility pattern**: Inter (1-1), PSV (2-1), Lyon (0-0), Manchester United (1-0 via own goal)
- **The Liverpool collapse**: a leg-by-leg breakdown of what the numbers actually show
- **Statistical analysis**: correlation matrix, distributions, efficiency comparisons

All charts are interactive (built with Plotly.js). Hover over any chart for details.

---

## Key findings

Barcelona's shot efficiency at home was **0.183**. Away from home it was **0.101**, less than half.

At Anfield specifically:
- Barcelona had *more* possession than in the first leg (57% vs 48%)
- Same number of shots on target in both legs (5)
- Leg 1: 3 goals from 12 shots. Leg 2: 0 goals from 8 shots
- Liverpool's shot efficiency flipped from 0.000 to 0.286

The correlation between possession and goals across these 12 matches: **r = +0.049**. Essentially nothing. Shots on target carried the real signal at r = +0.578.

Every away win and draw came down to a single moment (a Messi free-kick, a Shaw own goal, a penalty). The structure never dominated. At Anfield, there was no such moment.

---

## Data

All data is match-level and player-level statistics for Barcelona's 2018-19 UCL campaign, covering the group stage through the semi-finals.

Sources are public football statistics. No tracking data or event sequences.

---

## Running the notebook

```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook notebooks/barca_ucl_2019_analysis.ipynb
```

The notebook is already executed with all outputs saved.

---

Chack the datastory at : https://imaneoujja.github.io/barca-ucl-18-19/
