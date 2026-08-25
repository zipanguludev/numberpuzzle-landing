# numberpuzzle-landing

Sito del gioco **Operandi (Number Puzzle)**, servito via GitHub Pages:
<https://zipanguludev.github.io/numberpuzzle-landing/>

Contenuti:

- `index.html` — landing con presentazione del gioco: hero, screenshot,
  griglia delle feature, badge store ufficiali, meta Open Graph per le
  anteprime social.
- `gioca.html` — pagina di atterraggio dei link condivisi dall'app
  (`AppInfo.shareUrl` nel repo dell'app, sovrascrivibile via Remote
  Config `share_url`): redirect automatico allo store giusto su
  Android/iOS/iPadOS, badge per desktop e piattaforme ignote. Il link
  Play porta `referrer=utm_source%3Dshare` per contare in Play Console
  gli install arrivati dalle condivisioni (la landing usa
  `utm_source%3Dlanding`).
- `privacy-policy.html` — privacy policy linkata dalle schede store e dal
  dialog impostazioni dell'app (URL in `AppInfo.privacyPolicyUrl` nel repo
  dell'app).
- `terms.html` — termini di servizio, stesso collegamento in-app.
- `assets/` — favicon e touch icon (derivate da `icon-512.png`, il
  master), `og-image.jpg` per le anteprime social (dalla feature graphic
  dello store), badge ufficiali Google Play / App Store, screenshot
  `screen-*.jpg` catturati dal simulatore con
  `integration_test/landing_shots_test.dart` nel repo dell'app.
- `.nojekyll` — Pages serve i file così come sono, senza build Jekyll.

Gli URL di `gioca.html` e delle pagine legali sono referenziati dall'app
pubblicata (e i link già condivisi restano nel mondo per sempre): **non
rinominare i file** senza aggiornare `lib/core/app_info.dart` nel repo
`numberpuzzle` e le schede store.

Per rifare gli screenshot a gioco cambiato: nel repo dell'app,
`flutter test integration_test/landing_shots_test.dart -d <simulatore>`
e uno watcher esterno che scatta `xcrun simctl io booted screenshot` a
ogni marker `SHOT>>nome` stampato dal test (le istruzioni sono in testa
al test stesso).
