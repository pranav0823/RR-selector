# Pressure Reliability Ratings: interactive dashboard

A single-page dashboard for the SupeRR Selector Season 2, Round 1 submission.
It is one self-contained file, `index.html`. All data and the win-probability model are embedded, so there is no build step and no server.

## What is in it
- A match-situation simulator: set runs, balls and wickets and see the Pressure Index, win probability and what each outcome of the next ball would do.
- The top 10 batters and bowlers under pressure, with bootstrap intervals.
- An explorer for every eligible player (98 batters, 98 bowlers): search, filter, sort, and open any player for the full record.
- What each player would add to Rajasthan Royals, with availability for the IPL 2027 auction and an obtainable match.
- How pressure is defined, the main findings, and the robustness checks.

## Run it locally
Open `index.html` in a browser.

## Deploy on Vercel through GitHub
1. Create a new GitHub repository and add `index.html` and this `README.md` at the top level.
2. `git add . && git commit -m "Pressure dashboard" && git push`
3. In Vercel choose **Add New > Project** and import the repository.
4. Leave the framework preset as **Other**, with no build command and no output directory.
5. Select **Deploy**. Vercel serves `index.html` at the project URL.

## Notes
- The page loads the Archivo typeface from Google Fonts and falls back to the system font if that is blocked.
- To rebuild after changing the analysis, run `s6_dashboard_data.py` and `s7_build_dashboard.py` from the code bundle.
