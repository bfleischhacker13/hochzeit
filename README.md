<html lang="de">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Hochzeit · Villa Giulia</title>
  <meta name="description" content="Hochzeitsinformationen · Villa Giulia" />

  <!-- ============================================================
       COLORS & FONTS — edit these CSS variables to restyle the page
       ============================================================ -->
  <style>
    :root {
      --yellow:        #f5c63a;   /* stripe color */
      --cream:         #fbf3d8;   /* alternating stripe color */
      --card:          #e8b8a8;   /* salmon card background */
      --text:          #c43a25;   /* red headline / body text */
      --button:        #c43a25;   /* button fill */
      --button-text:   #ffffff;
      --stripe-width:  56px;      /* width of one yellow + one cream stripe */
      --card-radius:   4px;
      --max-width:     980px;     /* page content max width */
    }

    * { box-sizing: border-box; }

    html { scroll-behavior: smooth; }

    body {
      margin: 0;
      font-family: "Source Sans Pro", "Helvetica Neue", Arial, sans-serif;
      color: var(--text);
      line-height: 1.55;
      background-color: var(--cream);
      background-image: repeating-linear-gradient(
        90deg,
        var(--yellow) 0,
        var(--yellow) calc(var(--stripe-width) / 2),
        var(--cream) calc(var(--stripe-width) / 2),
        var(--cream) var(--stripe-width)
      );
    }

    /* ---------- Top anchor nav ---------- */
    nav.top-nav {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(6px);
      background: rgba(251, 243, 216, 0.92);
      border-bottom: 1px solid rgba(196, 58, 37, 0.15);
    }
    nav.top-nav ul {
      list-style: none;
      margin: 0;
      padding: 12px 16px;
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 8px 24px;
      max-width: var(--max-width);
      margin: 0 auto;
    }
    nav.top-nav a {
      color: var(--text);
      text-decoration: none;
      font-weight: 600;
      font-size: 0.95rem;
      letter-spacing: 0.04em;
      text-transform: uppercase;
      padding: 4px 2px;
      border-bottom: 2px solid transparent;
      transition: border-color 0.2s ease;
    }
    nav.top-nav a:hover { border-bottom-color: var(--text); }

    /* ---------- Layout ---------- */
    main {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 48px 24px 80px;
    }

    section {
      scroll-margin-top: 80px;       /* so anchor jumps clear the sticky nav */
      margin-bottom: 36px;
    }

    .card {
      background: var(--card);
      border-radius: var(--card-radius);
      padding: 48px 56px;
      text-align: center;
    }

    /* On wide screens, show Fragebogen + Informationen side-by-side
       (matching the PDF's two-column page).                          */
    .two-col {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 36px;
    }
    @media (max-width: 760px) {
      .two-col { grid-template-columns: 1fr; }
      .card    { padding: 36px 28px; }
      main     { padding: 24px 14px 60px; }
    }

    h1, h2 {
      font-family: "Source Sans Pro", "Helvetica Neue", Arial, sans-serif;
      font-weight: 700;
      color: var(--text);
      letter-spacing: 0.02em;
      margin: 0 0 24px;
    }
    h1 { font-size: 2.4rem; text-transform: uppercase; }
    h2 { font-size: 1.9rem; text-transform: uppercase; }

    p { margin: 0 0 16px; }

    a { color: var(--text); }

    /* ---------- Big call-to-action button ---------- */
    .btn {
      display: inline-block;
      background: var(--button);
      color: var(--button-text);
      text-decoration: underline;
      font-weight: 700;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      padding: 16px 36px;
      margin-top: 12px;
      border-radius: 2px;
      transition: transform 0.15s ease, filter 0.15s ease;
    }
    .btn:hover { transform: translateY(-1px); filter: brightness(1.05); }

    /* ---------- Intro hero ---------- */
    .hero {
      text-align: center;
      padding: 64px 32px 24px;
    }
    .hero h1 {
      font-size: 2.8rem;
    }
    .hero .subtitle {
      font-size: 1.15rem;
      opacity: 0.85;
    }

    /* ---------- Footer ---------- */
    footer {
      text-align: center;
      padding: 24px 16px 40px;
      color: var(--text);
      opacity: 0.7;
      font-size: 0.85rem;
    }
  </style>
</head>

<body>

  <main>

    <!-- ========== 1 · INTRO ========== -->
    <section id="intro" class="hero">
      <h1>Buongiorno</h1>
      <p class="subtitle">Hochzeit von Teresa &amp; Benedikt </br>
      11.-13. September 2026</p>
    </section>

    <!-- ========== 2 & 3 · FRAGEBOGEN + DRESSCODE (side-by-side) ========== -->
    <div class="two-col">

      <section id="fragebogen" class="card">
        <h2>Fragebogen</h2>
        <p>
          Bitte füllt uns den kurzen Fragebogen bis 11. Juni aus,
          damit wir alle Details final planen können.
        </p>
        <a class="btn" href="https://forms.gle/WrqTDdghRBZXCGFN6" target="_blank" rel="noopener">Zum Fragebogen</a>
      </section>

      <section id="dresscode" class="card">
        <h2>Dresscode</h2>
        <p>
          <!-- EDIT: replace this placeholder with your actual dresscode -->
          Freitag 11. September - Zeremonie: Dolce Vita<br>
          Samstag 12. September - Pizza Party: Italo Disco<br>
        </p>
        <p style="margin-top: 28px;">
          Inspiration findet ihr auf unserem Pinterest Board:
        </p>
        <a class="btn" href="https://pin.it/6V2pGQUNS" target="_blank" rel="noopener">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="18" height="18"
               style="vertical-align: -3px; margin-right: 8px;" fill="currentColor" aria-hidden="true">
            <path d="M12 0C5.373 0 0 5.372 0 12c0 5.084 3.163 9.426 7.627 11.174-.105-.949-.2-2.405.042-3.441.218-.937 1.407-5.965 1.407-5.965s-.359-.719-.359-1.782c0-1.668.967-2.914 2.171-2.914 1.023 0 1.518.769 1.518 1.69 0 1.029-.655 2.568-.994 3.995-.283 1.194.599 2.169 1.777 2.169 2.133 0 3.772-2.249 3.772-5.495 0-2.873-2.064-4.882-5.012-4.882-3.414 0-5.418 2.561-5.418 5.207 0 1.031.397 2.138.893 2.738a.36.36 0 0 1 .083.345l-.333 1.36c-.053.22-.174.267-.402.161-1.499-.698-2.436-2.889-2.436-4.649 0-3.785 2.75-7.262 7.929-7.262 4.163 0 7.398 2.967 7.398 6.931 0 4.136-2.607 7.464-6.227 7.464-1.216 0-2.359-.631-2.75-1.378l-.748 2.853c-.271 1.043-1.002 2.35-1.492 3.146C9.57 23.812 10.763 24 12 24c6.627 0 12-5.373 12-12C24 5.372 18.627 0 12 0z"/>
          </svg>
          Zum Pinterest Board
        </a>
      </section>

    </div>

    <!-- ========== 4 · INFORMATIONEN ========== -->
    <section id="informationen" class="card">
      <h2>Informationen</h2>
      <p>
        Falls ihr noch nicht gebucht habt, können wir die
        folgenden Unterkünfte empfehlen:<br />
        Hotel Elisabeth Due:
        <a href="https://www.hotelelisabethdue.it/" target="_blank" rel="noopener">hotelelisabethdue.it</a><br />
        Siri Hotel Fano:
        <a href="https://www.sirihotelfano.it/" target="_blank" rel="noopener">sirihotelfano.it</a><br />
        Camping:
        <a href="http://www.sostacamperilrospo.it/" target="_blank" rel="noopener">sostacamperilrospo.it</a><br />
        Für größere Gruppen bietet sich auch Airbnb sehr gut an.
        Auch hier helfen wir gerne bezüglich Unterkunftswahl.
      </p>
      <p>
        Meldet euch aber gerne auch direkt bei uns, falls wir und
        das Villa Giulia Team euch bei der Organisation von
        Unterkunft, Transfers vor Ort oder Rahmenprogramm
        unterstützen können.
      </p>
      <p>
        Falls ihr Interesse an einem Flughafentransfer habt
        (Bologna, Rimini, Ancona), bitte meldet euch bis
        spätestens 11. Juni mit uns (inklusive Flugnummer und
        Personenanzahl).
      </p>
      <p>
        Die Villa Giulia ist nicht nur der Ort, an dem wir unsere
        Hochzeit feiern, sondern hat auch einen wunderschönen
        Garten inklusive Pool, der allen Gästen bis 20 Uhr zur
        Verfügung steht.
      </p>
    </section>

  </main>

  <footer>
    Villa Giulia
  </footer>

</body>
</html>
