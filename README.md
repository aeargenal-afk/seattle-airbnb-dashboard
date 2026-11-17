# Seattle Airbnb Market Overview (Tableau)

An interactive Tableau dashboard on 2016 Airbnb data for Seattle. It shows what drives nightly prices, which zipcodes are the most expensive and how revenue moved through the year.

**[View the live dashboard on Tableau Public](https://public.tableau.com/app/profile/andres.argenal/viz/AirbnbFullProject_17949463504650/SeattleAirbnbOverview)**

[![Seattle Airbnb Market Overview](https://public.tableau.com/static/images/Ai/AirbnbFullProject_17949463504650/SeattleAirbnbOverview/1.png)](https://public.tableau.com/app/profile/andres.argenal/viz/AirbnbFullProject_17949463504650/SeattleAirbnbOverview)

## Key figures

| Metric | Value |
|---|---|
| Total revenue (2016) | $98.3M |
| Average nightly price | $129 |
| Listings | 2,873 |

## Key findings

- **Price rises steadily with size.** The average nightly price goes from $96 for one bedroom to $585 for six. Each extra bedroom adds roughly $65-$135.

| Bedrooms | Avg. nightly price | Listings |
|---|---|---|
| 1 | $96.2 | 1,811 |
| 2 | $175.4 | 483 |
| 3 | $249.7 | 206 |
| 4 | $315.4 | 55 |
| 5 | $450.0 | 20 |
| 6 | $584.8 | 5 |

- **The market is mostly small homes.** One-bedroom listings make up about 70% of the listings with one to six bedrooms. Listings with four bedrooms or more are only about 3%.
- **Location changes the price a lot.** The average price ranges from about $65 a night in the cheapest zipcode (98125) to about $207 in the most expensive one (98134), a gap of roughly 3x.
- **Revenue grew through the year.** Weekly revenue roughly doubled (+108%), from about $1.0M in the first week of January to about $2.1M at the end of December. Most of the growth came between January and late spring.

## What I did

1. **Data model.** Connected the Listings and Calendar tables and related them on the listing ID, so prices per night (Calendar) could be combined with listing details (Listings).
2. **Worksheets.**
   - Average price per bedroom (bar chart) plus a count of listings per bedroom (table).
   - Weekly revenue across 2016 (line chart) with the percent change from the first week.
   - Average price per zipcode (map shaded by price) and the same values as a sorted bar chart.
   - KPI row: total revenue, average nightly price and number of listings.
3. **Dashboard.**
   - Title, KPI row and four charts in one view.
   - The map works as a filter: clicking a zipcode updates the KPIs and every other chart.
   - Cleaned up axis titles, number formats (revenue in millions) and colours, and excluded listings with no zipcode from the zipcode chart.

## How to use it

1. Open the [live dashboard](https://public.tableau.com/app/profile/andres.argenal/viz/AirbnbFullProject_17949463504650/SeattleAirbnbOverview).
2. Click a zipcode on the map to filter the whole dashboard to that area.
3. Click it again (or press Esc) to go back to all of Seattle.

## Files

The workbook is hosted on Tableau Public: open the live dashboard and use the download button to get the `.twbx` file. The screenshot above is served by Tableau Public, so it always shows the latest version.

## Tools

Tableau Public: relationships between tables, bar/line/map charts, number formatting, dashboard filter actions.

## Credits

The dataset and the original walkthrough come from Alex The Analyst's Tableau project ([Airbnb Listings 2016 dataset on Kaggle](https://www.kaggle.com/datasets/alexanderfreberg/airbnb-listings-2016-dataset)). I extended the tutorial version with a KPI row, a price-shaded map that filters the dashboard, and the findings above.

## Author

Andres Argeñal
