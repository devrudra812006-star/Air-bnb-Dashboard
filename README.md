# Global Airbnb Performance Dashboard

A multi-page data analysis dashboard built on real Airbnb listing data across 10 global cities. The goal was simple: cut through the noise and figure out what's actually happening with listings, reviews, pricing, and trust — without drowning in spreadsheets.

---

## What's in the Data

The dataset covers **279,712 listings** across **10 cities**, from **182,024 hosts**, with over **5.3 million reviews** and **144 distinct property types**. It's a lot. The dashboard breaks it into four focused views.

---

## Dashboard Pages

### 1. New Listings Over Time

Airbnb's growth story, plotted across four property types (private room, entire place, hotel room, shared room) from 2008 to 2021.

The chart splits into five phases — Introduction, Growth, Maturity, Decline, and COVID-19 — and you can see them play out clearly. Listings peaked around 2015 and then pulled back. Two things happened: local governments started tightening short-term rental rules in 2016-17, and Airbnb turned profitable during the same stretch. Then 2018 brought a second wave of growth, which COVID cut short in 2019-2020.

Entire Place listings dominated, with Private Rooms a distant second. Hotel Rooms and Shared Rooms barely register on the chart — a footnote, not a trend.

---

### 2. Market Share by City + Pricing + Ratings

**Market share:**
Paris, New York, and Sydney together account for close to half of all listings and 48% of reviews. Paris alone leads the pack. One reason: hotel rooms in Paris run about twice what Airbnb charges, which pushes more travelers toward the platform.

The Pareto curve overlaid on the bar chart makes the concentration obvious — the top three cities carry the first 48% of cumulative share before the others even get going.

**Pricing (global averages):**
- Hotel room: $800
- Entire place: $673
- Shared room: $580
- Private room: $462

**Ratings:**
The ratings table lets you toggle between an overall view and a breakdown by category (Accuracy, Cleanliness, Communication, Location, Value). Mexico City consistently scores at or near the top. Hong Kong and Istanbul sit at the lower end, particularly on cleanliness and value.

---

### 3. Overall Ratings View

Same page, different toggle. Instead of the category breakdown, this view shows a single average rating bar per city, sorted low to high.

Mexico City leads at 94.8. Hong Kong is last at 89.7. What's interesting is the gap isn't huge — the bottom of the list is still solidly rated. The spread across all 10 cities is about 5 points, which says something about platform-wide quality floors.

---

### 4. Review Frequency, Seasonality, and Trust

**Review frequency:**
86.3% of reviewers wrote exactly one review. Another 10% wrote two or three. After that, the numbers drop off fast. One customer wrote 283 reviews — flagged in the data as a possible data error or a serial globe-trotter.

**Seasonality:**
The stacked area chart covers five cities (Mexico City, New York, Paris, Rome, Sydney) month by month. Paris dominates throughout, with particularly heavy concentration from spring through fall. Sydney's contribution is steadier across the year, which tracks with its southern-hemisphere seasons.

**Trust signals:**
66.9% of Airbnb hosts have both a verified identity and a profile photo — the strongest trust tier. Another 32.6% have a photo but no identity verification. Hosts with no photo and no verification account for just 0.1% of listings.

The takeaway: nearly every host on the platform has at least one trust signal. The fully anonymous host is nearly extinct.

---

## Tools Used

- **MySQL** — data storage, cleaning, and querying. Joins, aggregations, and filtering all happen here before anything touches a visual.
- **Excel** — intermediate data shaping, quick sanity checks, and preparing exports for Power BI.
- **Power BI** — all the visuals. Every chart, table, and toggle in the dashboard is built here on top of the cleaned data coming out of MySQL via Excel.

---

## Notes

- City scope: Paris, New York, Sydney, Rome, Rio de Janeiro, Istanbul, Mexico City, Bangkok, Cape Town, Hong Kong
- Time range: 2008–2021 (listing history); review data covers the same window
- Ratings are on a 0–100 scale in the overall view and 0–10 in the category breakdown
