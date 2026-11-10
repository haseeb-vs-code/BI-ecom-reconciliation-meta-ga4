<h1><b>Project Overview</b></h1>
This project focuses on data harmonization and pipeline engineering to connect top-of-funnel paid media performance with backend web analytics. By engineering a multi-key data blend, this dashboard spots data discrepancies, tracking pixel inflation, and paid traffic drop-off rates.

**Dashboard: https://datastudio.google.com/s/rryt944qjuQ**

<h2><b>Data Architecture & Tech Stack</b></h2>

**BI Platform:** Google Looker Studio

**Data Sources:** Meta Ads Manager (Paid Acquisition) and Google Analytics 4 (Behavioral Analytics)

**Data Modeling:** Implemented a multi-key Left Outer Join using Date and Campaign Name as composite join dimensions.

**Schema Optimization:** Designed custom schemas to remove redundant join dimensions and clean up structural null values.

<h2><b>Executive Insights & Strategic Impact</b></h2>

- **The 32.1% Traffic Leak:** Uncovered a gap where nearly one-third of paid Meta Link Clicks (539 clicks) never registered as GA4 Sessions (366 sessions). This highlights a clear need to optimize mobile site-load speeds and compress page images.

- **Click-to-Session Match Rate by Audience:** Cold prospecting campaigns (New_Targeting) had the lowest match rate at 54.55%, while retargeting campaigns ranged from 70% to 92%. One possible explanation is that returning users are more willing to wait for a slow page to load, but the gap could also come from accidental clicks, bot traffic, ad blockers, or users declining cookie consent before GA4 records the session. A next step would be to compare match rates against page-load times by campaign to test which explanation holds.

- **Funnel Optimization:** Isolated a core bottleneck where cold prospecting spend successfully drives top-of-funnel clicks but results in a 0% purchase conversion rate. Based on this data, the immediate business recommendation is to shift budget into the high-performing retargeting campaigns to protect ROAS.
