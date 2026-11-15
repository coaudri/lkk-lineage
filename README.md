# Lambda Kappa Kappa lineage practice app

Open `index.html` in a browser. No install, account, or internet connection is required. Narrow the browser window to preview the phone layout.

Features: pledge-line directory, member search, season filters, year sorting, chronological timeline, line rosters, and member profile dialogs. The interface adapts to phones and larger screens.

This is a mobile-friendly browser prototype, not a packaged iOS or Android application. There is no authentication, server, database, or editing feature.

## Data

`lineage.json` is the editable source roster. The same data is embedded in `index.html` to allow opening the app directly without a server. After changing the JSON, replace the contents of the HTML script element with id `roster` with the updated JSON.

Records follow the supplied names and sequence, with spacing and quotation punctuation normalized. Sequence does not imply official line numbers. The timeline connects chronological pledge-line records; no individual mentor relationships have been inferred. The 2004 line retains all 16 supplied members.

## Suggested practice exercises

1. Add a line and update the embedded roster.
2. Add editable member biographies.
3. Add member photographs with consent.
4. Package the interface for iOS and Android once the prototype works as desired.

## Chapter events

`events.html` is the second page, linked from the lineage navigation. Upcoming, past, and all views support event search. No event details have been supplied yet.

To add events, edit the JSON array in the script element with id `event-data`. Each event accepts `title`, `start` (an ISO timestamp including UTC offset), optional `end`, `timeZone` (default America/Chicago), `location`, `category`, `description`, `url`, and `linkLabel`. Start-only events move to the past at their start time; provide an end time to retain ongoing events in Upcoming.
