# Online economics seminars

A list of free economics seminar series and research webinars you can join online, and their
upcoming talks. It is the data behind EconGoat's online seminar calendar.

Every talk is read from its series' own page, or from the series' own announcements: never from
an aggregator. Only dates the organizers have published are listed.

## Files

| File | What it is |
| --- | --- |
| `econ-seminars.ics` | Every talk as a calendar file. Import it into Google Calendar, Outlook or Apple Calendar. |
| `econ-seminars.csv` | Every talk, one row each, with its time for the organizer, New York and London. |
| `econ-seminar-series.csv` | Every series: field, organizer, schedule, platform, how to join, and its next talk. |
| `seminars.json` | Both lists in one file, for programs. The CSVs and the calendar file are built from it. |

The CSVs are UTF-8 with a byte-order mark, so Excel opens them with accents intact.

## In `seminars.json`

`generated` is the date the talks were last refreshed. `series` lists each series: `id`,
`name`, `short`, `type` (Seminar series, Policy webinar or Conference livestream), `field`,
`organizer`, `platform`, `schedule`, `status` (Active, Between seasons or Annual), `url` (its own
page), `registration`, `reg_url`, `join_info`, `open_to`, `notes` and `access`.

`talks` lists each talk: `series_id`, `date`, `end_date` (for an event of several days),
`start_utc` and `end_utc`, `local_orig` (the time as the organizer gives it), `tz`, `allday`,
`time_tba` (the date is known but not the time; such a talk is stored as the whole day),
`speaker`, `affiliation`, `title`, `link` (where to register or join), `access`,
`year_inferred` (the page gave no year), `source` (where the talk was read) and `id`.

`access` says how to get in:

| Value | Meaning |
| --- | --- |
| `direct` | The link is the meeting itself. |
| `open` | No sign-up needed. |
| `register` | Register first; the meeting link comes after. |
| `list` | Join the series' mailing list to get the link. |
| `email` | Email the organizers for the link. |
| `check` | See the event page for how to join. |

## Add a series or fix a talk

Open an issue with the series' own page (its schedule, not a news story about it), or a pull
request. Pull requests are copied by hand into the calendar's source, so a change here shows up
after the next refresh. A series belongs here if anyone can attend it online for free.

## Licence

This data is © EconGoat, licensed under
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)
(the full text is in `LICENSE`). You may copy, share and adapt it for non-commercial purposes,
if you credit EconGoat, link to this repository and the licence, say whether you changed it, and
share what you make from it under the same licence.

Talk titles are their speakers' own; dates, times and links are as the organizers publish them.
