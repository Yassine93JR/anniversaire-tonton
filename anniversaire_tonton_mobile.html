<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <title>NSI – Repérer un harceleur dans un réseau</title>
  <style>
    :root {
      --bg: #f4f6fb;
      --card: #ffffff;
      --accent: #e53935;
      --accent-soft: #ffebee;
      --text: #222;
      --muted: #666;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }

    body {
      background: radial-gradient(circle at top, #ffebee 0, #f4f6fb 40%, #f4f6fb 100%);
      color: var(--text);
      padding: 20px;
    }

    header {
      text-align: center;
      margin-bottom: 20px;
    }

    header h1 {
      font-size: 1.8rem;
      margin-bottom: 0.3rem;
    }

    header p {
      color: var(--muted);
      font-size: 0.95rem;
    }

    .container {
      max-width: 1000px;
      margin: 0 auto 40px auto;
    }

    .intro-box {
      background: var(--accent-soft);
      border-left: 4px solid var(--accent);
      padding: 16px 18px;
      border-radius: 8px;
      margin-bottom: 20px;
    }

    .intro-box strong {
      color: var(--accent);
    }

    .a4 {
      background: var(--card);
      width: 800px;
      max-width: 100%;
      margin: 20px auto;
      padding: 24px 26px;
      border-radius: 8px;
      box-shadow: 0 4px 14px rgba(0, 0, 0, 0.08);
      position: relative;
    }

    .a4::after {
      content: "A4";
      position: absolute;
      top: 10px;
      right: 14px;
      font-size: 0.7rem;
      color: var(--muted);
      opacity: 0.5;
    }

    .a4 h2 {
      font-size: 1.3rem;
      margin-bottom: 10px;
      color: var(--accent);
    }

    .a4 h3 {
      font-size: 1.05rem;
      margin: 14px 0 6px;
    }

    .a4 p {
      margin-bottom: 8px;
      line-height: 1.4;
      font-size: 0.95rem;
    }

    .schema {
      background: #fafafa;
      border: 1px dashed #ccc;
      border-radius: 6px;
      padding: 10px 12px;
      margin: 10px 0;
      font-family: "Courier New", monospace;
      font-size: 0.9rem;
      white-space: pre;
      overflow-x: auto;
    }

    .highlight {
      background: #fffde7;
      border-left: 3px solid #fdd835;
      padding: 8px 10px;
      border-radius: 4px;
      margin: 8px 0;
      font-size: 0.9rem;
    }

    .tag {
      display: inline-block;
      background: #e3f2fd;
      color: #1565c0;
      padding: 2px 8px;
      border-radius: 999px;
      font-size: 0.75rem;
      margin: 2px 4px 2px 0;
    }

    .table {
      width: 100%;
      border-collapse: collapse;
      margin: 10px 0;
      font-size: 0.9rem;
    }

    .table th,
    .table td {
      border: 1px solid #ddd;
      padding: 6px 8px;
      text-align: left;
    }

    .table th {
      background: #f1f1f1;
    }

    .footer {
      text-align: center;
      font-size: 0.8rem;
      color: var(--muted);
      margin-top: 20px;
    }

    @media print {
      body {
        background: #fff;
        padding: 0;
      }
      .a4 {
        box-shadow: none;
        border-radius: 0;
        margin: 0 auto 10mm auto;
        page-break-after: always;
      }
      header, .intro-box, .footer {
        display: none;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Repérer un harceleur dans un réseau</h1>
    <p>Étude de cas – NSI, réseaux, données, graphes et algorithmes</p>
  </header>

  <div class="container">
    <div class="intro-box">
      <p><strong>Problématique :</strong> Lorsqu’un élève reçoit des messages de harcèlement sur un réseau social ou un ENT, peut‑on identifier l’auteur grâce aux données techniques (IP, métadonnées, graphes de communication) tout en respectant la vie privée ?</p>
    </div>

    <!-- A4 1 : Cas concret -->
    <section class="a4">
      <h2>I. Cas concret : harcèlement dans un lycée</h2>
      <p>Un élève, que nous appellerons <strong>Samir</strong>, reçoit des messages anonymes insultants sur la messagerie interne du lycée (ENT). Les messages viennent d’un compte créé sous un faux nom :</p>
      <p><strong>« DarkWolf92 »</strong></p>
      <p>Le lycée veut savoir si l’auteur est un élève connecté au réseau interne.</p>

      <h3>Comment circule un message ?</h3>
      <p>Quand DarkWolf92 envoie un message à Samir :</p>
      <ul style="margin-left:18px; font-size:0.95rem; line-height:1.4;">
        <li>le message part de son ordinateur ;</li>
        <li>il passe par le réseau du lycée ;</li>
        <li>il arrive sur le serveur ENT ;</li>
        <li>puis il est transmis au compte de Samir.</li>
      </ul>

      <div class="schema">
DARKWOLF92
    │
    ▼
  RÉSEAU DU LYCÉE
    │
    ▼
 SERVEUR ENT
    │
    ▼
   SAMIR
      </div>

      <p>À chaque étape, des <strong>métadonnées</strong> sont enregistrées : adresse IP, heure, identifiant de session.</p>

      <span class="tag">Réseaux</span>
      <span class="tag">Serveurs</span>
      <span class="tag">Métadonnées</span>
    </section>

    <!-- A4 2 : IP et salle -->
    <section class="a4">
      <h2>II. Étape 1 : l’adresse IP comme indice</h2>
      <p>Les administrateurs du réseau consultent les journaux (logs) du serveur ENT. Ils voient que les messages de DarkWolf92 ont été envoyés depuis l’adresse IP :</p>
      <p><strong>10.0.12.45</strong></p>

      <p>Dans le lycée, chaque salle a une plage d’adresses IP :</p>
      <table class="table">
        <thead>
          <tr>
            <th>Salle</th>
            <th>Plage d’IP</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>101</td>
            <td>10.0.10.x</td>
          </tr>
          <tr>
            <td>102</td>
            <td>10.0.11.x</td>
          </tr>
          <tr>
            <td>103</td>
            <td>10.0.12.x</td>
          </tr>
          <tr>
            <td>104</td>
            <td>10.0.13.x</td>
          </tr>
        </tbody>
      </table>

      <p>L’adresse <strong>10.0.12.45</strong> correspond donc à la <strong>salle 103</strong>.</p>

      <div class="schema">
IP 10.0.12.45  →  Salle 103
      </div>

      <div class="highlight">
        Même si le compte est anonyme, l’adresse IP permet de savoir d’où vient le message dans le réseau.
      </div>

      <span class="tag">Adresses IP</span>
      <span class="tag">Routage</span>
    </section>

    <!-- A4 3 : Temps + emploi du temps -->
    <section class="a4">
      <h2>III. Étape 2 : analyse temporelle</h2>
      <p>Les messages de harcèlement ont été envoyés aux heures suivantes :</p>
      <ul style="margin-left:18px; font-size:0.95rem; line-height:1.4;">
        <li>8h42</li>
        <li>8h43</li>
        <li>8h44</li>
        <li>8h46</li>
      </ul>

      <p>On regarde l’emploi du temps de la salle 103 :</p>
      <table class="table">
        <thead>
          <tr>
            <th>Heure</th>
            <th>Classe présente</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>8h–10h</td>
            <td>Terminale NSI</td>
          </tr>
        </tbody>
      </table>

      <p>On peut donc en déduire que le harceleur est très probablement un élève de <strong>Terminale NSI</strong> présent en salle 103 à ce moment‑là.</p>

      <div class="highlight">
        En combinant l’adresse IP et l’horaire, on réduit fortement le nombre de suspects.
      </div>

      <span class="tag">Horodatage</span>
      <span class="tag">Logs</span>
    </section>

    <!-- A4 4 : Graphe de communication -->
    <section class="a4">
      <h2>IV. Étape 3 : graphe de communication</h2>
      <p>On représente les échanges de messages sous forme de <strong>graphe</strong> :</p>
      <ul style="margin-left:18px; font-size:0.95rem; line-height:1.4;">
        <li>Chaque élève = un nœud.</li>
        <li>Chaque message = une flèche (arête orientée).</li>
        <li>Les messages agressifs = flèches rouges.</li>
      </ul>

      <div class="schema">
A  →  Samir   (rouge)
B  →  Samir   (rouge)
C  →  Samir   (rouge)
D  →  Samir   (gris)
      </div>

      <p>On remarque que :</p>
      <ul style="margin-left:18px; font-size:0.95rem; line-height:1.4;">
        <li>l’élève A envoie beaucoup de messages agressifs à Samir ;</li>
        <li>ces messages sont très rapprochés dans le temps ;</li>
        <li>ils viennent tous de la même IP (10.0.12.45).</li>
      </ul>

      <div class="highlight">
        Dans le graphe, A apparaît comme le principal harceleur : il envoie de nombreuses flèches rouges vers Samir.
      </div>

      <span class="tag">Graphes</span>
      <span class="tag">Modélisation</span>
    </section>

    <!-- A4 5 : Algorithme simple -->
    <section class="a4">
      <h2>V. Étape 4 : algorithme de détection</h2>
      <p>On applique un algorithme simple pour repérer un comportement de harcèlement :</p>
      <p><strong>Idée :</strong> si un utilisateur envoie beaucoup de messages agressifs à la même personne en peu de temps, il devient suspect.</p>

      <div class="schema">
Pour chaque utilisateur U :
    compter les messages agressifs envoyés vers Samir
    si ce nombre > 3 en moins de 5 minutes :
        marquer U comme suspect
      </div>

      <p>Résultat de l’algorithme :</p>
      <ul style="margin-left:18px; font-size:0.95rem; line-height:1.4;">
        <li>U = A → suspect principal ;</li>
        <li>U = B, C, D → en dessous du seuil.</li>
      </ul>

      <div class="highlight">
        Cet algorithme est simple, mais il montre comment on peut utiliser des données et des seuils pour repérer un comportement anormal.
      </div>

      <span class="tag">Algorithmes</span>
      <span class="tag">Conditions</span>
      <span class="tag">Boucles</span>
    </section>

    <!-- A4 6 : Confirmation + conclusion -->
    <section class="a4">
      <h2>VI. Étape 5 : confirmation technique</h2>
      <p>Les administrateurs vérifient les journaux du serveur ENT :</p>
      <ul style="margin-left:18px; font-size:0.95rem; line-height:1.4;">
        <li>l’utilisateur A s’est connecté à 8h40 ;</li>
        <li>depuis l’IP 10.0.12.45 ;</li>
        <li>le compte « DarkWolf92 » a été créé à 8h41 ;</li>
        <li>les messages ont commencé à 8h42.</li>
      </ul>

      <p>Les données techniques confirment que :</p>
      <p><strong>A = DarkWolf92</strong></p>

      <h3>VII. Conclusion du cas</h3>
      <p>Grâce aux notions de NSI :</p>
      <ul style="margin-left:18px; font-size:0.95rem; line-height:1.4;">
        <li><strong>Réseaux</strong> : adresses IP, serveurs, ENT ;</li>
        <li><strong>Données</strong> : logs, horodatage, métadonnées ;</li>
        <li><strong>Graphes</strong> : représentation des échanges ;</li>
        <li><strong>Algorithmes</strong> : détection de comportements anormaux ;</li>
      </ul>
      <p>… on a pu identifier un harceleur qui pensait être anonyme.</p>

      <div class="highlight">
        L’informatique ne sert pas seulement à transporter des messages : elle permet aussi de protéger les utilisateurs et de repérer des comportements dangereux, à condition d’être utilisée avec prudence et dans le respect de la vie privée.
      </div>

      <h3>Notions NSI mobilisées</h3>
      <div class="schema">
MON SUJET
      │
 ┌────┼────┐
 │    │    │
RÉSEAUX DONNÉES ALGORITHMES
 │    │    │
IP  LOGS  GRAPHES
      │
  LUTTE CONTRE
  LE HARCÈLEMENT
      </div>
    </section>
  </div>

  <div class="footer">
    Site simple pour illustrer un exposé de Grand Oral NSI – HTML + CSS intégrés.
  </div>
</body>
</html>