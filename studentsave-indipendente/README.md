# StudentSave — versione indipendente

Web-app statica, senza account obbligatorio e senza server. Nessuna dipendenza da una piattaforma AI. Non serve installare Node, eseguire build o inserire credenziali.

## Link condivisibile con Netlify (consigliato)

1. Estrai lo ZIP: otterrai la cartella `studentsave-indipendente`.
2. Apri https://app.netlify.com/drop e accedi o crea un account Netlify.
3. Trascina la cartella che contiene `index.html` nell’area di caricamento.
4. Netlify assegna un indirizzo HTTPS del tipo `nome-sito.netlify.app`. Copia e invia quel link: i visitatori non devono creare account.
5. Per modificare il nome cerca la voce relativa al nome/dominio del progetto nel pannello Netlify. La disponibilità del nome dipende dal servizio. Eventuali limiti o costi dipendono dal piano scelto.

## Alternativa: GitHub Pages

1. Crea un repository GitHub pubblico, ad esempio `studentsave`.
2. Carica i file contenuti in questa cartella nella radice del repository: `index.html`, `app.js`, `styles.css`, `.nojekyll` e gli altri file.
3. In Settings → Pages scegli Deploy from a branch, branch `main` e cartella `/ (root)`, quindi Save.
4. Quando la pubblicazione termina, GitHub indica il link: normalmente `https://TUO-UTENTE.github.io/studentsave/`.
5. Il link è pubblico; non richiede account ai visitatori. Il codice in un repository pubblico è visibile.

Non caricare lo ZIP come unico file nel repository: devi caricare i file estratti. I percorsi relativi sono compatibili con le sottocartelle di GitHub Pages.

## Dati e funzionalità

- Ogni browser ha il proprio profilo locale. Email e nome sono dati del profilo, non un account verificato.
- Spese, budget e preferenze restano nel browser: non sono sincronizzati tra telefoni o computer.
- Il PIN facoltativo cifra i dati locali con AES-GCM e una chiave derivata tramite PBKDF2. Richiede HTTPS, disponibile su Netlify e GitHub Pages.
- Il PIN non può essere recuperato. Esporta i dati dal Profilo per conservarne una copia; il file esportato è in chiaro e non viene importato automaticamente.
- La cancellazione dei dati del browser elimina il profilo. L’app non invia email di recupero e non offre biometria nativa.
- Offerte, scadenze, volantini interni e punti sulla mappa sono esempi esplicitamente indicati. I collegamenti ai supermercati aprono i siti ufficiali.
- La mappa usa Leaflet e OpenStreetMap. Immagini e font provengono da servizi esterni; è necessaria una connessione Internet per queste risorse.
- Il GPS viene richiesto soltanto premendo il pulsante apposito.

## Modifiche

`index.html` è la pagina iniziale, `styles.css` contiene lo stile e `app.js` contiene l’app. Aggiorna i file e carica nuovamente la cartella sul servizio scelto. Non pubblicare file personali o esportazioni dei tuoi dati insieme al sito.
