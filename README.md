# Cardizine News Finder

A one-page tool for finding culture and general news stories from a particular day, or a range of days, to turn into Cardizine cards.

Open `index.html` in a browser. It is one self-contained file and needs no build step.

## Sources

| Source | How | Key |
| --- | --- | --- |
| Wikipedia | Reads `Portal:Current_events/<date>` for each day and lists every item with its category and citations | None |
| The Guardian | Open Platform content search, limited to culture, books, film, music, art, stage, TV, science, environment, technology, world, UK and US news | Free developer key from [open-platform.theguardian.com/access](https://open-platform.theguardian.com/access/) |
| New York Times | Archive API: one download per month, filtered to the chosen days. Falls back to Article Search | Free key from [developer.nytimes.com](https://developer.nytimes.com/get-started), with the Archive API and Article Search API enabled |
| BBC | No public archive API, so each day gets links to Wayback Machine snapshots of BBC News (front page, arts, science, world) and a Google search of the BBC limited to that date | None |

Add keys in **Settings**. They are stored only in your browser's local storage.

## Features

- Pick a day or range of days (up to 31), with buttons for today, yesterday, the last 7 days and stepping earlier or later
- Results grouped by day, with filters for source and topic, and search within the results
- Sport and party politics hidden by default. A sport or politics story that touches culture (film, music, Eurovision, museums, awards and so on) still shows. A checkbox shows everything
- Star stories to keep them in a shortlist, add a note to each, and copy the shortlist as text
- Links for every day to the Guardian's date pages, the NYT's Today's Paper and the Wikipedia day page
- The URL records the dates (for example `#2026-05-12/2026-05-18`), so a range can be bookmarked
- Light and dark themes, phone layout

## Notes

- Days are UK calendar days.
- The NYT allows about 5 requests a minute and 500 a day. The archive is one large file per month, so the first search in a month takes a few seconds; later searches in the same month reuse it until you reload the page.
- The Guardian developer key allows 500 requests a day.
