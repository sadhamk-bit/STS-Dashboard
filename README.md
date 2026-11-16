# STS Partner & Support Intelligence Dashboard

A browser-based dashboard for consolidating monthly Excel workbooks into partner, AUM, ticket, classification, escalation, empanelment, and service-quality views.

## Run it

Open `index.html` in a modern browser. For local development, serve the repository directory with any static web server (for example, `python -m http.server 8000`) and open `http://localhost:8000`.

## Import monthly data

1. Upload the October reference workbook first, followed by November, December, and later monthly workbooks.
2. The dashboard reads every sheet in each `.xlsx`, `.xls`, or `.csv` workbook and retains original row-level fields in **Data Explorer**.
3. Choose a month or **All months** to filter the dashboard. Data is saved in browser local storage and is not sent to a server.

The dashboard automatically recognizes common header variants for AUM, partner, ticket, classification, escalation, CSAT, FMR, and RWT. If a month is not present in the filename, you will be prompted to assign one. Since workbook layouts can vary, use Data Explorer to verify imported source rows and the detected metrics.

## Notes

- This is a static, client-side dashboard; each browser profile has its own local dataset. Export/backup is not currently included.
- Excel parsing and charts load from jsDelivr CDNs, so the first load requires internet access.
- Metric definitions are based on matching common column names; validate totals against your workbook's business definitions, especially when sheets contain overlapping summary/detail data.
