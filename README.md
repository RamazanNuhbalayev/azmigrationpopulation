# Azerbaijan Migration Population Analysis

*A visual and reproducible look at how many people **entered** and **left** Azerbaijan from 1970 to 2021.*

---

## 1 Why This Repository?

> **Policy** loves numbers — but spreadsheets can be overwhelming.
> This repo converts official Excel tables into clear charts so **decision‑makers, citizens and data folks** can all follow the story in minutes.

---

## 2 Data in Plain English

| What it is  | Details                                                                |
| ----------- | ---------------------------------------------------------------------- |
| Source file | `BeynəlxalqMiqrasiyaForGrid.xlsx` (open‑data, State Migration Service) |
| Years       | 1970‑1989 *(pre‑independence)* & 1990‑2021 *(post‑independence)*       |
| Columns     | Arrivals, Departures, Net change, City vs Rural splits                 |
| Granularity | Country‑level totals per year                                          |

Example rows (excerpt)fileciteturn5file0L1-L20
Negative values in **Net Change** mean more people left than arrived.

---

## 3 Key Questions Answered

1. **Is Azerbaijan a net sender or receiver of migrants over time?** (line chart)
2. **Which five foreign countries dominate recent inflows?** (ranked bars)
3. **How does migration differ between city and rural areas?** (dual‑axis plot)
4. **What changed before vs after 1990?** (side‑by‑side comparison)

*(Add screenshots in an `assets/` folder for your LinkedIn gallery.)*

---

## 4 Running the Notebook *(no requirements.txt needed)*

```bash
# Install minimal dependencies
pip install pandas plotly matplotlib openpyxl

# Launch Jupyter and open the notebook
jupyter notebook   # then open Migration_Analysis.ipynb
```

Even without a `requirements.txt`, the four libraries above are enough to reproduce every chart.

> **Tip for non‑coders:** simply scroll through the notebook on GitHub; static PNGs are saved below each code cell.

---

## 5 Behind the Scenes (for data people)

```text
📂 data/
   └── BeynəlxalqMiqrasiyaForGrid.xlsx
📒 Ölkə əhalisinin Miqrasiyasın analzi.ipynb
```

Core steps inside the notebook:

1. `pd.read_excel()` for two sheets ➜ concatenate.
2. `df.melt()` to long format ➜ tidy columns (`Year, Flow, Value`).
3. Compute **Net = Arrivals – Departures**.
4. Plot with **Plotly Express** and **Matplotlib**.
5. Export cleaned CSV + ready‑made PNGs.

Dependencies: `pandas · plotly · matplotlib · openpyxl` (all open‑source).

---

## 6 Next Steps

* [ ] Publish a Streamlit dashboard for real‑time filtering.
* [ ] Link migration trends to **remittance** data for economic context.
* [ ] CI workflow to refresh charts annually when new XLSX appears.

PRs & ideas are welcome — fork, branch, and open a pull request! 🚀

---

## 7 Author

**Ramazan Nuhbalayev**
Let’s connect on LinkedIn — questions and collaborations are encouraged.

> *Turning raw tables into insights so everyone — from ministers to students — can follow the people movement map.*
