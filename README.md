# numberpuzzle-landing

Sito del gioco **Operandi (Number Puzzle)**, servito via GitHub Pages:
<https://zipanguludev.github.io/numberpuzzle-landing/>

Contenuti:

- `index.html` — landing con presentazione del gioco (store badge placeholder
  finché le schede non sono pubbliche).
- `privacy-policy.html` — privacy policy linkata dalle schede store e dal
  dialog impostazioni dell'app (URL in `AppInfo.privacyPolicyUrl` nel repo
  dell'app).
- `terms.html` — termini di servizio, stesso collegamento in-app.
- `.nojekyll` — Pages serve i file così come sono, senza build Jekyll.

Gli URL delle pagine legali sono referenziati dall'app pubblicata: **non
rinominare i file** senza aggiornare `lib/core/app_info.dart` nel repo
`numberpuzzle` e le schede store.
