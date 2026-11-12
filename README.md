# ArabicNLP in numbers

An interactive dashboard of the **ArabicNLP / WANLP** conference series (2014 to today): papers, authors, citations, research themes and shared tasks, based on the conference's Google Scholar venue profile and the ACL Anthology.

**Live dashboard:** https://kamelgaanoun.github.io/arabicnlp-dashboard/
It is also embedded on the [SIGARAB website](https://www.sigarab.org/).

## What it shows

- **Papers & selectivity:** papers per edition, citations by edition, and main-track acceptance rates.
- **Community:** authors per edition, first-time vs returning authors, and team size.
- **Impact:** citations received per year, most cited papers, and most frequent authors. Author counts can use all authors, the first author only, or fractional counting.
- **Research themes:** topics, topic mix over time, methods and resources.
- **Shared tasks:** tasks per edition and the list of tasks.
- **All papers:** a searchable, sortable table, exportable to CSV.

Every chart responds to the filters: edition, paper type (main track, shared-task systems, task overviews), topic, and a free-text search on titles and authors. Light and dark modes are available.

## How it works

The whole dashboard is a single self-contained file, `index.html`. The data is embedded in it, so there is no server, database or build step. GitHub Pages serves the file as is.

Data sources:
- **Google Scholar** venue profile *Conference on Arabic Natural Language Processing (ArabicNLP, WANLP)*: the paper list, citation counts, h-index and citations per year.
- **ACL Anthology:** the complete author lists, where Scholar truncates them.
- **ArabicNLP organizers:** submission and acceptance numbers per edition.

## Updating after a new edition

The update tools are hidden on the published page. They appear when the file is opened locally, or when `#admin` is added to the URL.

1. Download `index.html` and open it locally in a browser (double-click). The **Update data** and **Download updated dashboard** buttons appear.
2. Click **Update data**. The dialog explains each input:
   - the BibTeX export of the Scholar venue profile;
   - the Scholar profile page, saved as "Web Page, complete", for citations, metrics and the citations-per-year history;
   - the acceptance figures for the new edition.
3. Check the paper types in the admin table and correct them if needed. Manual corrections are kept in all later updates.
4. Click **Download updated dashboard**. Rename the downloaded file to `index.html` and upload it to this repository (**Add file → Upload files → Commit changes**).

The live page and the SIGARAB embed show the new version within a minute or two, with no change needed on the website.

## Credits

- Original dashboard: **Wajdi Zaghouani**.
- Data import, additional indicators, redesign and maintenance: **Kamel Gaanoun**.
- The papers are added to the Scholar venue profile with [scholar-feeder](https://github.com/KamelGaanoun/scholar-feeder).
