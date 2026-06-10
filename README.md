<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>La Sauce Humanitaire — Association d'entraide à Vaulx-en-Velin</title>
<meta name="description" content="La Sauce Humanitaire, association loi 1901 à Vaulx-en-Velin : maraudes, colis alimentaires, soutien scolaire, entraide de proximité. Ouverte à tous, sans condition ni distinction.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Anton&family=Archivo:wght@400;500;600;700&family=Montserrat:wght@300;400&display=swap" rel="stylesheet">
<style>
  :root{
    --sauce:#E2401B;
    --sauce-fonce:#B92F10;
    --ink:#181512;
    --paper:#FFFFFF;
    --creme:#FBF9F6;
    --safran:#F2A33C;
    --trait:#E9E2D8;
    --gris:#6E675F;
  }
  *{margin:0;padding:0;box-sizing:border-box}
  html{scroll-behavior:smooth}
  body{
    font-family:'Archivo',system-ui,sans-serif;
    color:var(--ink);
    background:var(--paper);
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3{line-height:1.05}
  a{color:inherit}
  img,svg{display:block}
  .conteneur{max-width:1180px;margin:0 auto;padding:0 24px}
  .etiquette{
    font-size:12px;font-weight:600;letter-spacing:.22em;
    text-transform:uppercase;
  }
  :focus-visible{outline:3px solid var(--safran);outline-offset:3px}

  /* ---------- En-tête ---------- */
  header{
    position:sticky;top:0;z-index:50;
    background:var(--paper);
    border-bottom:1px solid var(--trait);
  }
  .barre{
    display:flex;align-items:center;justify-content:space-between;
    gap:24px;padding:14px 24px;max-width:1320px;margin:0 auto;
  }
  .logo-cadre{
    font-family:'Montserrat',sans-serif;font-weight:300;
    font-size:13px;letter-spacing:.28em;text-transform:uppercase;
    border:1.5px solid var(--ink);padding:9px 16px 8px;
    white-space:nowrap;text-decoration:none;color:var(--ink);
    transition:background .2s,color .2s;
  }
  .logo-cadre:hover{background:var(--ink);color:var(--paper)}
  nav ul{display:flex;gap:30px;list-style:none}
  nav a{
    text-decoration:none;font-weight:500;font-size:15px;
    padding-bottom:3px;border-bottom:2px solid transparent;
    transition:border-color .2s;
  }
  nav a:hover{border-color:var(--sauce)}
  .btn{
    display:inline-block;text-decoration:none;font-weight:700;
    font-size:15px;padding:13px 26px;border-radius:2px;
    transition:transform .15s,background .2s,color .2s,border-color .2s;
    border:2px solid transparent;cursor:pointer;
  }
  .btn:active{transform:scale(.97)}
  .btn-sauce{background:var(--sauce);color:#fff}
  .btn-sauce:hover{background:var(--sauce-fonce)}
  .btn-ink{background:var(--ink);color:#fff}
  .btn-ink:hover{background:#000}
  .btn-blanc{background:#fff;color:var(--ink)}
  .btn-blanc:hover{background:var(--creme)}
  .btn-contour{border-color:#fff;color:#fff}
  .btn-contour:hover{background:#fff;color:var(--sauce)}
  .menu-burger{display:none;background:none;border:0;cursor:pointer;padding:6px}
  .menu-burger span{display:block;width:24px;height:2px;background:var(--ink);margin:5px 0}

  /* ---------- Héros ---------- */
  .heros{background:var(--sauce);color:#fff;overflow:hidden}
  .heros-int{padding:88px 24px 0;max-width:1180px;margin:0 auto}
  .heros .etiquette{color:#FFD9CC;animation:monte .7s .05s both}
  .heros h1{
    font-family:'Anton',sans-serif;font-weight:400;
    font-size:clamp(56px,10.5vw,148px);
    text-transform:uppercase;letter-spacing:.01em;
    margin:18px 0 26px;max-width:11ch;
    animation:monte .7s .15s both;
  }
  .heros h1 .souligne{
    box-shadow:inset 0 -.16em 0 var(--ink);
  }
  .heros p.chapeau{
    font-size:clamp(17px,2vw,21px);max-width:620px;color:#FFEDE6;
    animation:monte .7s .3s both;
  }
  .heros .actions-cta{display:flex;gap:14px;flex-wrap:wrap;margin:36px 0 70px;animation:monte .7s .45s both}
  @keyframes monte{from{opacity:0;transform:translateY(26px)}to{opacity:1;transform:none}}

  .chiffres{
    border-top:1px solid rgba(255,255,255,.35);
    display:grid;grid-template-columns:repeat(4,1fr);
    max-width:1180px;margin:0 auto;
  }
  .chiffres div{
    padding:22px 24px;border-right:1px solid rgba(255,255,255,.35);
  }
  .chiffres div:last-child{border-right:0}
  .chiffres strong{
    font-family:'Anton',sans-serif;font-weight:400;font-size:30px;display:block;
  }
  .chiffres span{font-size:13px;color:#FFD9CC;letter-spacing:.08em;text-transform:uppercase}

  /* ---------- Bandeau défilant ---------- */
  .ticker{
    background:var(--ink);color:var(--paper);
    overflow:hidden;white-space:nowrap;padding:13px 0;
    border-bottom:1px solid var(--ink);
  }
  .ticker-piste{display:inline-flex;animation:defile 30s linear infinite}
  .ticker span{
    font-family:'Anton',sans-serif;font-size:17px;letter-spacing:.12em;
    text-transform:uppercase;padding:0 18px;
  }
  .ticker .sep{color:var(--safran)}
  @keyframes defile{from{transform:translateX(0)}to{transform:translateX(-50%)}}

  /* ---------- Sections ---------- */
  section{padding:90px 0}
  .tete-section{max-width:680px;margin-bottom:54px}
  .tete-section .etiquette{color:var(--sauce)}
  .tete-section h2{
    font-family:'Anton',sans-serif;font-weight:400;
    font-size:clamp(36px,5vw,58px);text-transform:uppercase;
    margin:12px 0 16px;
  }
  .tete-section p{color:var(--gris);font-size:17px}

  /* ---------- Actions ---------- */
  #actions{background:var(--creme)}
  .grille-actions{
    display:grid;grid-template-columns:repeat(2,1fr);gap:18px;
  }
  .carte{
    background:var(--paper);border:1px solid var(--trait);
    padding:30px 28px;display:flex;gap:22px;align-items:flex-start;
    transition:border-color .2s,transform .2s,box-shadow .2s;
    opacity:0;transform:translateY(22px);
  }
  .carte.visible{opacity:1;transform:none;transition:opacity .5s,transform .5s,border-color .2s,box-shadow .2s}
  .carte:hover{border-color:var(--sauce);box-shadow:0 10px 28px rgba(24,21,18,.07)}
  .carte .icone{
    flex:0 0 52px;height:52px;border:1.5px solid var(--ink);
    border-radius:50%;display:grid;place-items:center;color:var(--sauce);
  }
  .carte h3{font-size:20px;font-weight:700;margin:2px 0 8px}
  .carte .tag{
    font-size:11px;font-weight:600;letter-spacing:.18em;text-transform:uppercase;
    color:var(--sauce);
  }
  .carte p{font-size:15.5px;color:var(--gris)}

  /* ---------- L'asso ---------- */
  .deux-cols{display:grid;grid-template-columns:1.1fr .9fr;gap:70px;align-items:start}
  .citation{
    background:var(--ink);color:var(--paper);padding:42px 38px;
    position:sticky;top:110px;
  }
  .citation p{
    font-family:'Anton',sans-serif;font-size:clamp(24px,2.6vw,32px);
    text-transform:uppercase;line-height:1.25;
  }
  .citation p em{color:var(--safran);font-style:normal}
  .citation small{
    display:block;margin-top:20px;font-family:'Archivo';font-size:13px;
    letter-spacing:.18em;text-transform:uppercase;color:#B7B0A8;
  }
  .valeurs{list-style:none;display:grid;gap:0;margin-top:34px}
  .valeurs li{
    border-top:1px solid var(--trait);padding:22px 0;
    display:grid;grid-template-columns:140px 1fr;gap:18px;
  }
  .valeurs li:last-child{border-bottom:1px solid var(--trait)}
  .valeurs strong{font-family:'Anton',sans-serif;font-weight:400;font-size:19px;text-transform:uppercase;color:var(--sauce)}
  .valeurs span{color:var(--gris);font-size:15.5px}

  .equipe{margin-top:38px}
  .grille-equipe{display:grid;grid-template-columns:1fr 1fr;gap:14px}
  .membre{
    display:flex;align-items:center;gap:14px;
    border:1px solid var(--trait);padding:15px 18px;background:var(--paper);
    transition:border-color .2s;
  }
  .membre:hover{border-color:var(--sauce)}
  .membre .avatar{
    flex:0 0 46px;height:46px;border-radius:50%;
    background:var(--sauce);color:#fff;display:grid;place-items:center;
    font-family:'Anton',sans-serif;font-size:15px;
  }
  .membre strong{display:block;font-size:15.5px}
  .membre div span{font-size:13px;color:var(--gris)}

  /* ---------- Aider ---------- */
  #aider{background:var(--ink);color:var(--paper)}
  #aider .tete-section .etiquette{color:var(--safran)}
  #aider .tete-section p{color:#B7B0A8}
  .grille-aider{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
  .carte-aide{
    border:1px solid #3A352F;padding:34px 30px;display:flex;flex-direction:column;gap:14px;
    transition:border-color .2s;background:#1F1B17;
  }
  .carte-aide:hover{border-color:var(--safran)}
  .carte-aide h3{font-family:'Anton',sans-serif;font-weight:400;font-size:24px;text-transform:uppercase}
  .carte-aide p{color:#B7B0A8;font-size:15.5px;flex:1}
  .carte-aide .montant{color:var(--safran);font-weight:700;font-size:14px;letter-spacing:.1em;text-transform:uppercase}

  /* ---------- Contact / pied ---------- */
  #contact .deux-cols{align-items:center}
  .bloc-contact p{margin-bottom:14px;font-size:17px}
  .bloc-contact a{color:var(--sauce);font-weight:600;text-decoration:none}
  .bloc-contact a:hover{text-decoration:underline}
  .logo-final{
    font-family:'Montserrat',sans-serif;font-weight:300;
    letter-spacing:.3em;text-transform:uppercase;text-align:center;
    border:2px solid var(--ink);padding:26px 20px;font-size:clamp(14px,2.4vw,22px);
  }
  footer{
    background:var(--ink);color:#B7B0A8;font-size:13.5px;
  }
  footer .conteneur{
    display:flex;justify-content:space-between;gap:20px;flex-wrap:wrap;
    padding-top:26px;padding-bottom:26px;
  }
  footer a{color:#fff;text-decoration:none}
  footer a:hover{text-decoration:underline}

  /* ---------- Apparition au défilement ---------- */
  .revele{opacity:0;transform:translateY(24px);transition:opacity .6s,transform .6s}
  .revele.visible{opacity:1;transform:none}

  /* ---------- Réactif ---------- */
  @media (max-width:920px){
    .grille-actions,.grille-aider{grid-template-columns:1fr}
    .deux-cols{grid-template-columns:1fr;gap:40px}
    .grille-equipe{grid-template-columns:1fr}
    .citation{position:static}
    .chiffres{grid-template-columns:repeat(2,1fr)}
    .chiffres div:nth-child(2){border-right:0}
    nav{display:none}
    nav.ouvert{
      display:block;position:absolute;top:100%;left:0;right:0;
      background:var(--paper);border-bottom:1px solid var(--trait);
      padding:10px 24px 22px;
    }
    nav.ouvert ul{flex-direction:column;gap:16px}
    .menu-burger{display:block}
    section{padding:64px 0}
  }
  @media (max-width:560px){
    .barre{padding:12px 16px;gap:12px}
    .logo-cadre{font-size:10.5px;letter-spacing:.16em;padding:8px 10px}
    .barre .btn-sauce{display:none}
    .valeurs li{grid-template-columns:1fr;gap:6px}
    .citation{padding:30px 24px}
    .chiffres div{padding:16px 18px}
    .chiffres strong{font-size:24px}
  }
  @media (prefers-reduced-motion:reduce){
    *,.ticker-piste{animation:none!important;transition:none!important}
    .carte,.revele{opacity:1;transform:none}
    html{scroll-behavior:auto}
  }
</style>
</head>
<body>

<!-- ============ EN-TÊTE ============ -->
<header>
  <div class="barre">
    <a class="logo-cadre" href="#haut" aria-label="La Sauce Humanitaire — retour en haut">La Sauce Humanitaire</a>
    <nav id="nav-principale" aria-label="Navigation principale">
      <ul>
        <li><a href="#actions">Nos actions</a></li>
        <li><a href="#asso">Qui sommes-nous</a></li>
        <li><a href="#aider">Nous aider</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
    <div style="display:flex;align-items:center;gap:14px">
      <a class="btn btn-sauce" href="#aider">Faire un don</a>
      <button class="menu-burger" aria-label="Ouvrir le menu" aria-expanded="false" onclick="basculerMenu(this)">
        <span></span><span></span><span></span>
      </button>
    </div>
  </div>
</header>

<!-- ============ HÉROS ============ -->
<section class="heros" id="haut" style="padding:0">
  <div class="heros-int">
    <p class="etiquette">Association loi 1901 · Vaulx-en-Velin · Métropole de Lyon</p>
    <h1>On met la <span class="souligne">sauce</span>, pour de vrai.</h1>
    <p class="chapeau">Maraudes, colis alimentaires, soutien scolaire, visites aux isolés : de l'entraide de terrain, portée par des bénévoles du quartier. Ouverte à tous, sans condition ni distinction.</p>
    <div class="actions-cta">
      <a class="btn btn-ink" href="#aider">Devenir bénévole</a>
      <a class="btn btn-contour" href="#actions">Découvrir nos actions</a>
    </div>
  </div>
  <div class="chiffres">
    <div><strong>2021</strong><span>année de création</span></div>
    <div><strong>100&nbsp;%</strong><span>bénévoles</span></div>
    <div><strong>11</strong><span>maraudes par an</span></div>
    <div><strong>300+</strong><span>familles accompagnées</span></div>
  </div>
</section>

<!-- ============ BANDEAU DÉFILANT ============ -->
<div class="ticker" aria-hidden="true">
  <div class="ticker-piste" id="piste"></div>
</div>

<!-- ============ ACTIONS ============ -->
<section id="actions">
  <div class="conteneur">
    <div class="tete-section revele">
      <p class="etiquette">Ce qu'on fait, concrètement</p>
      <h2>Dix actions, un seul cap&nbsp;: l'entraide</h2>
      <p>Chaque action est menée par une équipe de bénévoles, financée par vos dons et ouverte à toute personne dans le besoin, d'où qu'elle vienne.</p>
    </div>
    <div class="grille-actions" id="grille-actions"><!-- cartes injectées --></div>
  </div>
</section>

<!-- ============ L'ASSO ============ -->
<section id="asso">
  <div class="conteneur deux-cols">
    <div class="revele">
      <div class="tete-section" style="margin-bottom:0">
        <p class="etiquette">Qui sommes-nous</p>
        <h2>Née à Vaulx, ouverte à tous</h2>
        <p>La Sauce Humanitaire est une association loi 1901 créée en 2021 à Vaulx-en-Velin. Pas de salariés, pas de structure lourde&nbsp;: un bureau de deux personnes, trois membres permanents et une quinzaine de bénévoles roulants chaque année, qui mettent leur temps au service de ceux que la vie bouscule, à Vaulx, à Lyon et au-delà.</p>
      </div>
      <ul class="valeurs">
        <li><strong>Dignité</strong><span>On aide sans juger ni trier&nbsp;: chaque personne est accueillie quelle que soit son origine, sa culture ou sa situation.</span></li>
        <li><strong>Proximité</strong><span>Nos actions partent du terrain. On connaît les rues, les cages d'escalier et les visages de ceux qu'on accompagne.</span></li>
        <li><strong>Transparence</strong><span>Fonctions 100&nbsp;% bénévoles, comptes présentés chaque année en assemblée générale&nbsp;: chaque euro va à l'action.</span></li>
      </ul>
      <div class="equipe">
        <p class="etiquette" style="color:var(--sauce);margin-bottom:16px">L'équipe</p>
        <div class="grille-equipe">
          <div class="membre">
            <span class="avatar">WM</span>
            <div><strong>Walid Moudoub</strong><span>Président</span></div>
          </div>
          <div class="membre">
            <span class="avatar">NE</span>
            <div><strong>Nassim El Kandoussi</strong><span>Vice-président</span></div>
          </div>
          <div class="membre">
            <span class="avatar">+3</span>
            <div><strong>Membres permanents</strong><span>Le noyau dur de l'asso</span></div>
          </div>
          <div class="membre">
            <span class="avatar">≈15</span>
            <div><strong>Bénévoles roulants</strong><span>Chaque année, sur le terrain</span></div>
          </div>
        </div>
      </div>
    </div>
    <aside class="citation revele">
      <p>«&nbsp;La sauce, chez nous, c'est <em>l'énergie qu'on met</em> quand quelqu'un a besoin d'un coup de main.&nbsp;»</p>
      <small>Walid Moudoub &amp; Nassim El Kandoussi, fondateurs</small>
    </aside>
  </div>
</section>

<!-- ============ AIDER ============ -->
<section id="aider">
  <div class="conteneur">
    <div class="tete-section revele">
      <p class="etiquette">Rejoindre le mouvement</p>
      <h2>Trois façons de mettre la sauce</h2>
      <p>Don ponctuel, deux heures par mois ou adhésion à l'année&nbsp;: chaque geste fait tourner les actions.</p>
    </div>
    <div class="grille-aider">
      <div class="carte-aide revele">
        <h3>Faire un don</h3>
        <p>5&nbsp;€ financent un repas chaud en maraude, 20&nbsp;€ un colis alimentaire complet pour une famille. Don déductible des impôts à hauteur de 66&nbsp;%.</p>
        <span class="montant">Dès 5&nbsp;€ · reçu fiscal</span>
        <a class="btn btn-sauce" href="#contact">Je donne</a>
      </div>
      <div class="carte-aide revele">
        <h3>Devenir bénévole</h3>
        <p>Maraude du jeudi soir, aide aux devoirs le mercredi, tri du vestiaire le samedi&nbsp;: deux heures par mois suffisent pour changer une semaine.</p>
        <span class="montant">2&nbsp;h / mois minimum</span>
        <a class="btn btn-blanc" href="#contact">Je m'engage</a>
      </div>
      <div class="carte-aide revele">
        <h3>Adhérer à l'asso</h3>
        <p>Devenez membre actif pour 20&nbsp;€ par an&nbsp;: vous votez en assemblée générale et participez aux décisions de l'association.</p>
        <span class="montant">20&nbsp;€ / an</span>
        <a class="btn btn-blanc" href="#contact">J'adhère</a>
      </div>
    </div>
  </div>
</section>

<!-- ============ CONTACT ============ -->
<section id="contact">
  <div class="conteneur deux-cols">
    <div class="bloc-contact revele">
      <div class="tete-section" style="margin-bottom:24px">
        <p class="etiquette">Contact</p>
        <h2>On vous répond vite</h2>
      </div>
      <p>📍 Vaulx-en-Velin (69120) — Métropole de Lyon</p>
      <p>✉️ <a href="mailto:contact@lasaucehumanitaire.fr">contact@lasaucehumanitaire.fr</a></p>
      <p>💼 <a href="https://www.linkedin.com/company/76243706/" target="_blank" rel="noopener">La Sauce Humanitaire</a> sur LinkedIn</p>
      <p style="color:var(--gris);font-size:15px;margin-top:22px">Dons en nature (vêtements, denrées non périssables, produits d'hygiène)&nbsp;: écrivez-nous pour connaître les prochains points de collecte.</p>
    </div>
    <div class="logo-final revele">La Sauce Humanitaire</div>
  </div>
</section>

<footer>
  <div class="conteneur">
    <span>© 2026 La Sauce Humanitaire — Association loi 1901, Vaulx-en-Velin</span>
    <span><a href="https://www.linkedin.com/company/76243706/" target="_blank" rel="noopener">LinkedIn</a> · <a href="#haut">Haut de page ↑</a></span>
  </div>
</footer>

<script>
  // ----- Données des actions -----
  const ACTIONS = [
    {tag:"Rue", titre:"Maraudes du soir",
     desc:"Chaque jeudi, distribution de repas chauds, boissons, duvets et surtout d'écoute auprès des personnes sans abri de Lyon et Villeurbanne.",
     icone:"bol"},
    {tag:"Alimentaire", titre:"Colis alimentaires",
     desc:"Des paniers de produits frais et secs préparés et livrés chaque mois aux familles en difficulté de Vaulx-en-Velin et des communes voisines.",
     icone:"panier"},
    {tag:"Éducation", titre:"Soutien scolaire",
     desc:"Aide aux devoirs du CP à la 3e, encadrée par des étudiants bénévoles, deux soirs par semaine pendant l'année scolaire.",
     icone:"livre"},
    {tag:"Vêtements", titre:"Vestiaire solidaire",
     desc:"Collecte, tri et redistribution gratuite de vêtements, chaussures et manteaux, avec une grande braderie solidaire avant chaque hiver.",
     icone:"cintre"},
    {tag:"Hygiène", titre:"Kits dignité",
     desc:"Trousses complètes — savon, brosse à dents, rasoir, protections périodiques — distribuées en rue et dans les foyers d'hébergement.",
     icone:"goutte"},
    {tag:"Santé & lien", titre:"Visites aux malades et aux aînés",
     desc:"Présence régulière à l'hôpital, en EHPAD et à domicile pour rompre l'isolement des personnes malades ou âgées du quartier.",
     icone:"coeur"},
    {tag:"Démarches", titre:"Permanence administrative",
     desc:"Un écrivain public bénévole chaque semaine pour aider aux dossiers CAF, logement, santé et démarches en ligne.",
     icone:"stylo"},
    {tag:"Lien social", titre:"Grandes tablées de quartier",
     desc:"Des repas partagés ouverts à tous, plusieurs fois par an, pour recréer du lien entre voisins, générations et cultures.",
     icone:"table"},
    {tag:"International", titre:"Urgences internationales",
     desc:"Collectes ponctuelles pour les populations touchées par les crises — séismes, inondations — et parrainage d'orphelins via des partenaires locaux.",
     icone:"globe"},
    {tag:"Jeunesse", titre:"Jeunesse & sport",
     desc:"Tournois de foot, sorties découvertes et mentorat pour encadrer, valoriser et inspirer les jeunes de Vaulx-en-Velin.",
     icone:"ballon"}
  ];

  // ----- Icônes SVG (trait minimal) -----
  const ICONES = {
    bol:'<path d="M4 11h16a8 8 0 0 1-16 0Z"/><path d="M9 7c0-1.5 1.5-1.5 1.5-3M14 7c0-1.5 1.5-1.5 1.5-3"/>',
    panier:'<path d="M5 9h14l-1.5 9.5a1 1 0 0 1-1 .9h-9a1 1 0 0 1-1-.9L5 9Z"/><path d="M8 9l3-5M16 9l-3-5"/>',
    livre:'<path d="M4 5a2 2 0 0 1 2-2h13v16H6a2 2 0 0 0-2 2V5Z"/><path d="M4 19a2 2 0 0 1 2-2h13"/>',
    cintre:'<path d="M12 6a2 2 0 1 1 2-2"/><path d="M12 6 3.5 12.5A1.5 1.5 0 0 0 4.4 15h15.2a1.5 1.5 0 0 0 .9-2.5L12 6Z"/>',
    goutte:'<path d="M12 3s6 6.5 6 11a6 6 0 1 1-12 0c0-4.5 6-11 6-11Z"/>',
    coeur:'<path d="M12 20s-7-4.5-9-9a4.6 4.6 0 0 1 8-4.4L12 8l1-1.4a4.6 4.6 0 0 1 8 4.4c-2 4.5-9 9-9 9Z"/>',
    stylo:'<path d="m5 19 1-4L16.5 4.5a2.1 2.1 0 0 1 3 3L9 18l-4 1Z"/><path d="M14 7l3 3"/>',
    table:'<path d="M3 9h18M6 9v8M18 9v8M9 13h6"/>',
    globe:'<circle cx="12" cy="12" r="9"/><path d="M3 12h18M12 3c2.5 2.7 2.5 15.3 0 18-2.5-2.7-2.5-15.3 0-18Z"/>',
    ballon:'<circle cx="12" cy="12" r="9"/><path d="M12 8l3.5 2.6-1.3 4.2h-4.4L8.5 10.6 12 8ZM12 3v5M5 7.5l3.5 3.1M19 7.5l-3.5 3.1M7 20l2.8-3.2M17 20l-2.8-3.2"/>'
  };

  // ----- Injection des cartes -----
  const grille = document.getElementById('grille-actions');
  ACTIONS.forEach(a=>{
    const el = document.createElement('article');
    el.className = 'carte';
    el.innerHTML = `
      <div class="icone" aria-hidden="true">
        <svg width="26" height="26" viewBox="0 0 24 24" fill="none"
             stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round">${ICONES[a.icone]}</svg>
      </div>
      <div>
        <span class="tag">${a.tag}</span>
        <h3>${a.titre}</h3>
        <p>${a.desc}</p>
      </div>`;
    grille.appendChild(el);
  });

  // ----- Bandeau défilant (contenu doublé pour boucle parfaite) -----
  const piste = document.getElementById('piste');
  const mots = ACTIONS.map(a=>a.titre);
  const seq = mots.map(m=>`<span>${m}</span><span class="sep">✶</span>`).join('');
  piste.innerHTML = seq + seq;

  // ----- Apparition au défilement -----
  const obs = new IntersectionObserver(entries=>{
    entries.forEach(e=>{
      if(e.isIntersecting){e.target.classList.add('visible');obs.unobserve(e.target);}
    });
  },{threshold:.12});
  document.querySelectorAll('.carte,.revele').forEach(el=>obs.observe(el));

  // ----- Menu mobile -----
  function basculerMenu(btn){
    const nav = document.getElementById('nav-principale');
    const ouvert = nav.classList.toggle('ouvert');
    btn.setAttribute('aria-expanded', ouvert);
  }
  document.querySelectorAll('#nav-principale a').forEach(l=>
    l.addEventListener('click',()=>document.getElementById('nav-principale').classList.remove('ouvert'))
  );
</script>
</body>
</html>
