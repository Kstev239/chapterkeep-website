# chapterkeep-website

The website of the Chapterkeep app, served by GitHub Pages at https://chapterkeep.de.

Plain HTML and CSS, no build step. German pages at the root, English pages under `/en/`.

- `index.html`, `en/index.html`: the landing pages, edited here.
- `konto-loeschen/`, `en/delete-account/`: how to delete the account, edited here. Google Play asks
  for this URL in the Data safety form.
- `hilfe/`, `datenschutz/`, `nutzungsbedingungen/`, `impressum/` and `en/help/`, `en/privacy/`,
  `en/terms/`, `en/imprint/`: **generated** from the FAQ and the legal texts of the app
  (github.com/Kstev239/story_sum), don't edit them here. After changing the texts in the app repo,
  run there (with this repo next to it):

  ```bash
  flutter test tool/website/export_legal_pages.dart --dart-define=OUT=../chapterkeep-website
  ```

  and commit the changed pages here.
- `CNAME`: the custom domain for GitHub Pages. `.nojekyll`: serves the files as they are.
- `fonts/`: Literata Bold for the headings (SIL Open Font License, `fonts/Literata-OFL.txt`).

No cookies, no tracking, no external resources, see the privacy policy.
