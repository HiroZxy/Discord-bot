# Analyse concurrentielle — Stimulicat / Instinct Basket

**Date des observations :** 6 octobre 2026 (extractions TrendTrack entre 19 h 21 et 19 h 35 UTC)
**Référence étudiée :** stimulicat.com — fiche TrendTrack `81116494-e148-4241-8e2e-cf93b67381d4` (workspace `w-s-workspace-BG9HrBQ`)
**Objectif retenu (par défaut) :** lancer une boutique rentable, documentée en *build in public* pour une audience débutante.
**Budget, contraintes, produit imposé :** non renseignés → valeurs par défaut appliquées (produit le plus poussé en publicité ; comparaison européenne large ; budgets présentés en scénarios non autorisés).

> **Légende des niveaux de preuve utilisés dans tout le document**
> **[FAIT]** observé directement dans une source (connecteur ou résultat de recherche) · **[ESTIM. OUTIL]** estimation calculée par un outil tiers (TrendTrack, benchmark) · **[VENDEUR]** affirmation du vendeur (publicité, page) · **[HYPOTHÈSE]** déduction ou recommandation de l'analyste · **[N.D.]** non disponible.

---

## 0. Décision en une page

| Question | Réponse | Confiance |
|---|---|---|
| Produit moteur | **Instinct Basket** : panier rond tressé en corde (coton selon les fiches marketplace), coussin amovible, jouet balle/queue, vendu **79,95 $** sur stimulicat.com. Il concentre ≈ 86 % des annonces à portée mesurée (275/320) et la totalité des 20 annonces les plus diffusées. | Élevée |
| Appréciation du shop | Machine publicitaire efficace (452 annonces actives, ~2,13 M d'impressions UE sur 30 j), mais produit **générique** (copies à 17–24 $ sur Amazon/Walmart, ~7,6 $ en promo sur AliExpress) vendu via des **allégations fragiles** (« lime les griffes », « absorbe les phéromones de façon permanente », « vets », faux prix barré, « we're going out of business »). | Élevée |
| Concurrence | Le concept a été **cloné et traduit dans presque tous les grands marchés UE entre juin et octobre 2026** : ≥ 30 annonceurs repérés. Les plus forts aujourd'hui : **Nidora / vittasa.com (ES)**, **Fellnest / renuevo.de (DE)**, **Elvori (NL)**, **Aristocatto (IT)**, **SoftPawsCo (FR/DE)**. | Élevée (sur l'échantillon) |
| Où la concurrence directe est-elle la plus faible ? | Parmi les marchés couverts : **Portugal, Danemark, Tchéquie, Hongrie, Roumanie, Grèce** (aucun clone localisé trouvé avec deux familles de requêtes), puis **Pologne** (un seul petit test arrêté). | Moyenne (risque de faux négatifs liés aux déclinaisons grammaticales) |
| Marché prioritaire pour un premier test | **Italie** — signal de demande indirect le plus fort de l'UE (54 % de la portée UE de Stimulicat, diffusion continue d'avril à octobre 2026, en anglais), grande population féline, CPM modéré ; concurrence locale réelle mais très récente (2 clones actifs démarrés fin septembre / début octobre). | Moyenne-faible |
| Alternatives | 1) **Pologne** (fenêtre de faible concurrence, CPM bas, mais prix plafond plus bas et signal de demande faible) · 2) **Allemagne** (plus grand marché félin, un seul clone établi, CPM plus élevé, exigences de confiance/conformité). | Faible à moyenne |
| À éviter pour le 1er test | **Espagne** (Nidora en forte accélération), **Pays-Bas** (Elvori + 2e zone UE de Stimulicat), **France** (≥ 10 tests en 4 mois, message saturé), **US/UK anglophones** (terrain de Stimulicat + ancrage prix marketplace). | Moyenne |
| Premier test proposé | Italie, positionnement **« le griffoir qu'il adopte vraiment — sans promesse miracle »**, 3 angles × 2 hooks, page produit vs page éditoriale, décisions pilotées par le CPA d'équilibre (≈ 16 € dans le scénario central). | — |

**Réserves majeures :** (1) aucune page web externe n'a pu être ouverte (réseau de l'environnement bloquant) → prix, compositions et politiques des concurrents restent partiellement non vérifiés ; (2) la portée publicitaire mesurée ne couvre que l'UE (transparence DSA) — la diffusion US de Stimulicat, probablement majoritaire, est invisible ; (3) les estimations de ventes TrendTrack sont **incohérentes avec le trafic** (voir §2.4) ; (4) le cycle de cette tendance semble déjà avancé (vague de clones), la fenêtre peut se refermer vite.

---

## 1. Méthode, périmètre et couverture

### 1.1 Sources et outils
| Source | Usage | Paramètres essentiels | Statut |
|---|---|---|---|
| TrendTrack `brief_competitor` | Snapshot boutique, produits, emails | competitor = 81116494-…, max_products 10, max_emails 15 | OK |
| TrendTrack `search_ads` | Annonces du domaine stimulicat.com | search_in=domain ; tri reach (total, min_reach=1, 17 pages = 329 annonces) ; tri reachDelta7d ; filtres langue et pays | OK (page 17 : 9 annonces de portée ≤ 3 non agrégées) |
| TrendTrack `lookup_filter_ids` (landing_pages) | Landing pages du domaine | scope_domain=stimulicat.com | OK |
| TrendTrack `scan_ad` | Hooks, transcriptions, historique d'impressions de la page | collations 1041624258462083, 1001091596275726, 1405875501065526 | OK |
| TrendTrack `search_ads` (concurrence) | Familles de requêtes traduites (texte d'annonce + URL) | voir 1.3 | OK |
| TrendTrack `find_similar_shops`, `search_advertisers`, `lookup`, `search_shops` | Boutiques similaires, pages liées, fiches concurrents | — | OK (similar shops = hors sujet, cf. §4) |
| Recherche web (WebSearch) | Composition, prix publics, avis, réglementation, paiements, CPM, démographie féline | — | OK (résumés de moteur) |
| Ouverture de pages (WebFetch / curl) | Fiches produit, landing pages, Trustpilot, Loox | — | **Accès impossible** : politique réseau de l'environnement (proxy 403 sur tous les domaines externes, y compris stimulicat.com et les CDN d'images) |

**Conséquences de l'accès bloqué :** aucune capture d'écran de site n'a pu être réalisée ; aucune vidéo n'a été visionnée ; les hooks « parlés » proviennent uniquement des **transcriptions automatiques TrendTrack** ; les avis et prix web proviennent de **résumés de moteur de recherche** (extraits rapportés, page non ouverte).

### 1.2 Fenêtres temporelles
- Annonces : toute l'histoire indexée (premières annonces juin 2025) ; tendances 7 j / 30 j selon les champs TrendTrack `reachDelta7d` / `reachDelta30d`.
- Impressions quotidiennes de la page Stimulicat : 2025-07-01 → 2026-10-06 (le 2026-09-24 est manquant — trou de collecte).
- Trafic et ventes estimées : fenêtre « 30 derniers jours » de TrendTrack au 2026-10-06.

### 1.3 Familles de requêtes concurrentielles (homogènes, traduites)
| Famille | Exemple FR | Traductions utilisées |
|---|---|---|
| F1 – Texte d'annonce « corde naturelle + chat + griffes » | `corde naturelle` + `chat` + `griffes` (mode ET) | EN natural rope/cat/nails · DE Naturseil/Katze/Krallen · ES cuerda natural/gato/uñas · IT corda naturale/gatto/unghie · NL natuurlijk touw/kat/nagels · PL lina/kot/pazury · PT corda natural/gato/unhas · SE naturrep/katt/klor · DK naturreb/kat/kløer · CZ lano/kočka/drápy · RO frânghie/pisic/gheare · HU kötél/macska/karm · EL σχοινί/γάτα/νύχια |
| F2 – « panier griffoir » (texte ou URL) | `panier griffoir`, `panier-griffoir` (URL) | DE Kratzkorb · ES cesta rascadora / rascador+cesta · IT graffiatoio+cesta · NL krabmand · PL drapak+kosz · PT arranhador+cesto · CZ škrabadlo+košík · HU kaparó+kosár · RO zgârietoare+coș · DK kradse+kurv |
| F3 – URL produit générique | `rope-cat-bed`, `scratching-basket` | — |

Tri : portée totale décroissante (page 1, 20 annonces) **et** nouveauté (page 1, 20 annonces) pour FR, DE, ES ; portée seule pour les autres. **Déséquilibre assumé :** FR/DE/ES ont reçu 2 tris + requêtes F2 ; les petits marchés 2 familles seulement. Les marchés **non couverts** : Finlande, Norvège, Slovaquie, Bulgarie, Croatie, Slovénie, pays baltes, Irlande (couverte uniquement via l'anglais), Autriche et Belgique (couvertes via l'allemand, le français et le néerlandais, sans requête dédiée), Suisse (hors UE). Canada et Australie non étudiés en profondeur (références : ciblages de Stimulicat).

---

## 2. Identifier le produit moteur

### 2.1 Échantillon et critères
- 4 926 annonces indexées pour le domaine (tous statuts) **[FAIT]** ; 329 ont une portée UE > 0, dont 320 agrégées **[FAIT]**.
- Classement par produit d'après l'URL de destination : **Instinct Basket 275** (265 URL explicites + 10 vers `advertorial-territorial-stress-2`, très probablement le panier **[HYPOTHÈSE]**), **Explorer Harness 44**, autre 1 **[FAIT]**.
- Landing pages (lookup TrendTrack) : la fiche `instinct-basket-meet-the-first-research-backed-natural-territory-for-indoor-cats` porte **31 annonces actives**, la version best-sellers 5, l'Instinct Mat 6 ; toutes les autres sont à 0 actif **[FAIT]**.
- Les 20 annonces à plus forte portée cumulée et les 20 à plus forte accélération sur 7 jours renvoient toutes au panier **[FAIT]**.

**Conclusion :** produit moteur = **Instinct Basket**, sans ambiguïté. Produit secondaire en test : **Instinct Mat** (tapis griffoir, 49,95 $, 6 annonces actives). Le harnais (Explorer Harness) était le produit d'acquisition historique (juin 2025 – janvier 2026) **[FAIT, d'après dates d'annonces]**.

### 2.2 Fiche produit reconstituée
| Élément | Valeur | Niveau |
|---|---|---|
| Format | Panier rond tressé, oreilles de chat, coussin amovible, balle/queue jouet | FAIT (titres marketplace) |
| Matière | « Handwoven natural rope » (Stimulicat) ; « 100 % natural cotton rope », « four-strand rope » (résumés de pages) | VENDEUR / extrait moteur |
| Tailles | M ≈ 40–42 cm ; une version 18 × 18 × 6 pouces citée | Extrait moteur (non vérifié) |
| Prix | 79,95 $ ; prix « barré » 159,95 $ (« tonight only ») ; coussin additionnel 29,95 $ | FAIT (TrendTrack) / VENDEUR |
| Livraison | « FREE Worldwide Shipping » | VENDEUR |
| Garantie | « 45-Day Cat Approval Guarantee » (annonces 2026) ; « 30-day guarantee » dans d'anciennes transcriptions | VENDEUR — incohérence |
| Preuve sociale | « ★★★★★ 20,000+ sold » (CTA) ; Loox 3 120 avis 4,5/5 (autre capture : 1 941) ; Trustpilot 4,0/5 (157 avis) ou 4,3 (83) | VENDEUR / extraits moteur, avis **globaux boutique** |
| Public visé | « cat moms », propriétaires de chats d'intérieur, multi-chats | FAIT (copies) |

### 2.3 Périmètre concurrentiel défini avant recherche
- **A – Produit identique confirmé :** panier rond tressé en corde de coton + coussin + jouet, caractéristiques documentées. → **Aucun concurrent n'atteint ce niveau** : les pages n'ont pas pu être ouvertes. Plusieurs sont *probablement* le même produit générique, sans preuve.
- **B1 – Concurrent direct comparable (clone d'angle) :** panier/« nid » en corde naturelle vendu sur la promesse griffes + territoire/odeur.
- **B2 – Même format, autre positionnement :** panier en corde de coton vendu comme lit/déco (boutiques catalogue, marketplaces).
- **C – Alternatives :** griffoirs carton/sisal en forme de lit, arbres à chat, diffuseurs de phéromones, coupe-griffes.
- **D – Hors sujet :** boutiques de harnais (proposées par « boutiques similaires »), autres produits Stimulicat.

### 2.4 Indicateurs de la boutique de référence
| Indicateur | Valeur | Niveau | Commentaire |
|---|---|---|---|
| Pays de création | US | ESTIM. OUTIL | — |
| Trafic mensuel | 49 703 visites (+7,3 % / 30 j) ; autre endpoint : 45 806 ; sous-domaine try.stimulicat.com : 26 177 | ESTIM. OUTIL | Écart entre endpoints |
| Pays visiteurs | US 93,9 %, ES 3,4 %, NL 1,0 %, DE 0,9 %, TR 0,8 % | ESTIM. OUTIL | Visiteurs ≠ clients |
| Ventes 30 j | 2 804 871 $ (fourchette 951 960 – 4 657 472 $) ; 37 236 unités | ESTIM. OUTIL | **Incohérent** : 37 k unités pour ~50–76 k visites impliquerait un taux de conversion irréaliste → à ne pas utiliser comme base |
| Annonces actives (page) | 452 | FAIT (TrendTrack) | — |
| Impressions UE de la page, 30 j | 2 134 672 | FAIT (transparence UE via TrendTrack) | Impressions ≠ personnes |
| Portée UE cumulée (somme des 320 annonces) | 9 781 658 | FAIT | Somme de portées : pas des personnes uniques |
| Pages publicitaires liées | Stimulicat (711004312088223), Cat Insider (756628667526995, 57 annonces actives, mêmes vidéos), SerenoSole (121397991056457, boutique serenosole.de, annonces DE juin 2025), Fera Pets (912141025320624, diffuse aussi solidgoldpet.com) | FAIT | À dédoublonner : même flux publicitaire |
| Réseaux | Instagram 679 abonnés (27/10/2025) → 9 675 (06/10/2026) ; 6 359 mentions J'aime Facebook ; page créée le 12/06/2025 | FAIT | — |

### 2.5 Trajectoire publicitaire (UE)
Impressions mensuelles de la page Stimulicat (somme quotidienne TrendTrack) **[FAIT]** :

| Mois | Impressions | Mois | Impressions |
|---|---|---|---|
| 2025-08 | 1 052 | 2026-03 | 1 309 |
| 2025-09 | 15 106 | 2026-04 | 275 129 |
| 2025-10 | 113 285 | 2026-05 | 572 412 |
| 2025-11 | 5 338 | 2026-06 | 1 376 670 |
| 2025-12 | 68 804 | **2026-07** | **3 438 574** (pic) |
| 2026-01 | 12 557 | 2026-08 | 2 400 063 |
| 2026-02 | 0 | 2026-09 | 1 994 848 (29 jours ; 24/09 manquant) |
| | | 2026-10 (1–6) | 366 594 |

7 derniers jours (30/09–06/10) : 392 568 ; 7 jours précédents (23–29/09, 6 jours de données) : 367 844. **Lecture :** montée en puissance avril → juillet 2026, puis décrue modérée mais diffusion toujours soutenue. Ceci concerne **uniquement l'UE**.

Répartition par **pays d'audience principal** (champ `mainCountry`, transparence UE) des 320 annonces **[FAIT]** :

| Pays principal | Annonces | Portée cumulée | Part |
|---|---|---|---|
| Italie | 25 | 5 311 571 | 54,3 % |
| Pays-Bas | 41 | 2 041 291 | 20,9 % |
| Pologne | 1 | 748 486 | 7,7 % |
| Hongrie | 7 | 466 106 | 4,8 % |
| (non renseigné) | 219 | 326 844 | 3,3 % |
| Allemagne | 2 | 230 328 | 2,4 % |
| France | 1 | 201 481 | 2,1 % |
| Espagne | 9 | 191 840 | 2,0 % |
| Grèce | 4 | 160 349 | 1,6 % |
| Belgique | 3 | 43 205 | 0,4 % |
| Suède / Roumanie / Portugal / Irlande | 1 / 2 / 2 / 3 | 30 139 / 18 889 / 5 900 / 5 229 | < 0,4 % chacun |

Les annonces ciblent 29 à 37 pays (UE + US, CA, AU, NZ). **Toutes les créations du panier sont en anglais** : les seules annonces non anglaises du domaine (29) datent de juin 2025 et portent sur le harnais (page SerenoSole, en allemand) **[FAIT]**. Formats : vidéo = 253 annonces et 97,6 % de la portée ; image 66 ; carrousel 1 **[FAIT]**.

**Estimation de dépense :** TrendTrack applique ≈ 9 $ pour 1 000 de portée (ex. 986 035 → 8 874 $) **[ESTIM. OUTIL]**. Formule : dépense ≈ portée × 9 / 1 000. C'est une simulation (CPM supposé, portée ≠ impressions), pas une dépense réelle.

**Contradictions de collecte signalées :** plusieurs annonces au statut « active » ont un `lastSeenAt` vieux de plusieurs mois (ex. 1842576809768760 : active, vue pour la dernière fois le 29/05/2026) ; l'outil emails indique 0 email/semaine sur 30 j alors qu'un email est daté du 29/09/2026.

---

## 3. Audit du shop de référence

### 3.1 Positionnement et persona
- **Positionnement [VENDEUR] :** « the first research-backed natural territory for indoor cats » — un panier présenté comme réponse biologique (écorce d'arbre, phéromones, griffes trop longues).
- **Persona publicitaire [FAIT, copies] :** propriétaire (souvent « cat mom ») d'un chat d'intérieur qui ignore les griffoirs, abîme le canapé, se mord les griffes ; secondairement foyers multi-chats.
- **Mécanisme avancé [VENDEUR] :** corde naturelle = texture d'écorce → « lime les griffes à chaque griffade » + « absorbe ses phéromones de façon permanente » → le chat revient « sans dressage ».

### 3.2 Parcours observés (reconstitués, non cliqués)
1. Annonce vidéo → **try.stimulicat.com** (pages éditoriales/listicles/advertorials : `wants-to-prevent-nail-pain-feature-benefit-territory-basket-79-95-offer`, `copy-of-wants-to-be-good-cat-parent-…`, `broad-feature-benefit-…`, `advertorial-scentandsafe`, `international-cat-day-offer-instinct-basket`, versions BFCM) → fiche produit → panier.
2. Annonce image « Not one to gatekeep » → **fiche produit directe** stimulicat.com.
3. Historique : variantes de fiche avec cadeaux (`…-free-organic-pillow`, NL `…-4-free-gifts`, `…-kopie`) aujourd'hui sans annonce active **[FAIT]**.

Le libellé « 79-95-offer » dans les URL suggère des tests de prix/offres par page **[HYPOTHÈSE]** ; un paramètre d'URL ne prouve ni une page différente ni un résultat.

**Non réalisé :** visite des pages, test mobile/desktop, vitesse, checkout (accès bloqué). **[N.D.]**

### 3.3 Offre, prix et confiance
- Prix 79,95 $ présenté comme réduction de 159,95 $ « tonight only », « 50 % off for new customers », « Free pillow included with your first order » **[VENDEUR]**.
- Livraison gratuite « worldwide », garantie 45 jours « If she does not claim it, full refund » **[VENDEUR]**.
- Avis Trustpilot (résumés de moteur) : plaintes sur **frais de retour élevés**, **délais internationaux**, colis compressé, coussin à l'odeur désagréable ; l'entreprise répond à 96 % des avis négatifs **[extraits moteur]**.

### 3.4 Emails capturés (15, du 29/04 au 29/09/2026) [FAIT]
Fréquence observée ≈ 2–3 par mois ; sujets : promotions jusqu'à −50 % (Spring, Fête nationale US, International Cat Day), livraison gratuite, contenus pédagogiques (« Why Does the Litter Box Smell Keep Coming Back? », « Real talk about scratching »), relationnel (« You got paid. They've been waiting »). Rôle probable : newsletters de réactivation et de cross-sell (FreshGuard, Instinct Mat). **Aucune conclusion possible** sur les flows automatisés ou le réachat.

### 3.5 Incohérences et points de vigilance
| Point | Observation | Risque |
|---|---|---|
| Prix de référence | « $159.95 down to $79.95 tonight only » répété depuis des mois | Pratique interdite dans l'UE si 159,95 n'est pas le prix le plus bas des 30 jours précédents (art. 6 bis directive 98/6/CE, Omnibus ; CJUE C-330/23) |
| Fausse rareté | « We're going out of business » (ann. 1417965509787687, 1513547650376688), « almost sold out », « handwoven one at a time, demand outpaces » alors que le produit est disponible en masse | Pratique commerciale trompeuse ; défiance |
| Allégations santé | « files her nails », « no clipping, no vet visits », « she is in pain », « Vets who see this every week… », « research-backed » | Non étayées ; les ressources vétérinaires indiquent que griffer retire les couches mortes mais **ne remplace pas la coupe** chez le chat d'intérieur (SF SPCA, Purina AU) |
| Garantie | 45 j dans les annonces récentes, 30 j dans d'anciennes | Confusion client |
| Preuve sociale | « 20,000+ sold » ; avis Loox globaux boutique | Avis non spécifiques au produit |
| Personae | Pages « Cat Insider », vidéos en voix de « propriétaire » | Témoignages potentiellement scénarisés **[HYPOTHÈSE]** |

### 3.6 Forces, faiblesses, enseignements
- **Forces :** volume de créations (≥ 4 926 annonces), itération rapide de hooks sur un même script, mécanisme simple et visuel, offre forte (garantie, livraison, cadeau), pages éditoriales dédiées par angle.
- **Faiblesses :** produit commoditisé (copies marketplace à 17–24 $), message en anglais pour toute l'Europe, allégations et urgences exposées juridiquement, avis négatifs sur retours/délais.
- **Réutilisable (sans copier) :** structure problème → mécanisme → démonstration → garantie ; segmentation des landing pages par angle ; vidéo dominante ; foyers multi-chats comme sous-segment.

---

## 4. Cartographie des concurrents

*Signaux = annonces TrendTrack de l'échantillon (familles F1/F2/F3), dates = première/dernière vue, portée = somme des portées UE des annonces de l'échantillon (pas des personnes uniques). « Actif » = au moins une annonce active au 05–06/10/2026.*

### 4.1 B1 — Clones d'angle (même format, même promesse griffes/territoire)

| Marque (page) | Domaine | Marché constaté (preuve) | Annonces échantillon / actives | Portée échantillon | Δ 7 j | Période | Statut |
|---|---|---|---|---|---|---|---|
| **Nidora** (Junga, 590247237507990) | vittasa.com | ES (mainCountry ES ; ciblage ES) | 16 / 16 (page : 72 actives, 1 253 054 portée 30 j) | 1 139 562 | +389 760 | 12/09 → 05/10/2026 | **Actif, en forte accélération** |
| **Fellnest** (Mindful.Insider 868687526335524 + Kathrin Gesmayer 946488275218209) | renuevo.de | DE | 18 / 3 | ~359 605 | +34 691 | 19/07 → 06/10/2026 | Actif |
| **Elvori** (670768856121471) | elvori.nl | NL | 12 / 4 (page : 68 actives) | 135 660 | +31 760 | 05/09 → 05/10/2026 | Actif |
| **Panier Amara** (Furanza 391140380749947) | support.get-novera.com | FR | 11 / 0 | 107 419 | 0 | 14/08 → 11/09/2026 | Arrêté |
| **Aristocatto** (« Gattedrale ») | aristocatto.com | IT | 16 / 4 (page : 10 actives) | 82 994 | +66 133 | 23/09 → 05/10/2026 | **Actif, récent** |
| Cosalia | cosalia-home.com | ES | 4 / 0 | 45 558 | 0 | 29/08 → 09/09/2026 | Arrêté |
| Comodea | comodea-home.com | IT | 2 / 0 | 37 367 | 0 | 10/09 → 17/09/2026 | Arrêté |
| Elanzo (« PurrNest ») | elanzo.nl | NL | 4 / 0 | 32 144 | 0 | 29/06 → 15/07/2026 | Arrêté |
| SoftPawsCo (Reisena 477138132139130) | softpawsco.com | FR + DE | ~13 / ~11 (page : 65 actives) | ~32 000 | ~+18 000 | 27/09 → 05/10/2026 | Actif, récent |
| Wooflyx | wooflyx.com | DE/NL (URL traduite de Stimulicat) | 4 / 0 | ~21 000 | 0 | 29/06 → 28/07/2026 | Arrêté |
| Felyra (Habicat IT) | myfelyra.com | IT | 2 / 2 | 12 688 | +8 114 | 03/10 → 05/10/2026 | Actif, tout récent |
| Zevlo | le-panier-que-les-chats-raffolent.zevlo.co | FR | 2 / 0 | 10 650 | 0 | 16/06 → 12/07/2026 | Arrêté |
| Loria (« Instinct mand ») | trouwepoot.nl | NL/BE | 2 / 0 | 10 182 | 0 | 15/07 → 08/09/2026 | Arrêté |
| ÉVEZA | éveza.com (xn--veza-9oa.com) | FR | 1 / 0 | 7 990 | 0 | 26/08 → 01/09/2026 | Arrêté (908 visites/mois estimées) |
| Isba&Co (« le panier instinct ») | isba-co.com | FR | 1 / 0 | 6 503 | 0 | 14 → 15/08/2026 | Arrêté |
| naevi (Maluchron 1024693717398503, « gniazdo instynktu ») | naevi.pl | PL | 7 / 0 | 5 593 | +3 478 | 26/09 → 02/10/2026 | Arrêté (test) |
| Meowlia | meowlia.com | FR | 1 / 0 | 3 437 | 0 | 26 → 27/07/2026 | Arrêté |
| Fleecky | fleecky.com | FR | 1 / 0 | 3 282 | 0 | 01 → 02/09/2026 | Arrêté |
| Zarpa™ (Silenxio) | silenxio.com | ES | ~10 / ~10 | < 3 000 | faible | 30/09 → 05/10/2026 | Actif, test (boutique créée le 20/06/2026, vend aussi un anti-ronflement) |
| WizzFit (page « Mara Tabitha ») | wizzfit.com | UK | ~18 / 0 | < 3 000 | 0 | 16 → 17/08/2026 | Arrêté |
| PawFabric (Milky Fabrics, « panier-griffoir-instinct ») | paw-fabric.com | FR/BE | 5 / 0 | < 4 000 | 0 | 29 → 31/07/2026 | Arrêté — la boutique vend désormais des gouttes pour chien |
| Sensicat (page « Sara Andersson ») | shopmonura.com | SE | 5 / 0 | 373 | 0 | 22 → 23/07/2026 | Arrêté |
| Shop Veralae | aveloriae.com | FR | 6 / 6 | 836 | 0 | 05 → 06/10/2026 | Actif, tout récent |
| OlyPet | olypet.fr | FR | 4 / 4 | 0 | 0 | 30/09 → 06/10/2026 | Actif, tout récent |
| Cosylane (Cosylane / Elaya) | cosylanehome.com/de | DE | 20 / 20 | 0 | 0 | 03 → 06/10/2026 | Actif, tout récent (page : 270 annonces actives tous produits) |
| Auravos | auravos.store | EN (hors UE probable) | 3 / 3 | 0 | 0 | 03 → 05/10/2026 | Actif, récent |
| Cuddlecom | cuddlecom.com | EN | 2 / 0 | 0 | 0 | 02 → 04/10/2026 | Arrêté |
| Mon Adorable Félin (« panier-pour-chat-griffoir ») | monadorablefelin.com | FR | ~20 / 0 | ~2–8 k par annonce (page : 649 701 portée totale) | — | 29/10 → 21/11/2025 | Arrêté — matière non confirmée (B) |
| *Réf. hors Europe :* Pet Heaven (« Cat Nest ») | petheaven.cl | CL | — | — | — | 10/2026 | Actif |
| *Réf. hors Europe :* NaturaPurr | naturapurr.com | MX | — | — | — | 10/2026 | Actif |

**Différences avec la référence :** toutes reprennent le même mécanisme (corde « écorce », griffes limées, phéromones) et souvent **des traductions quasi littérales** des annonces Stimulicat (ex. Nidora : « Esto es lo que le pasa a un gato cuyo dueño ignora su necesidad de rascar… » = traduction du script n°1 ; Fellnest : « Das hier würde mit einer Katze passieren… » ; Furanza : « N'achetez pas le panier Amara si vous aimez votre chat… »). Garanties observées : Nidora 90 j, Fellnest 30 j, Amara 30 j, Zarpa 45 j **[VENDEUR]**. Prix Nidora vu via moteur : 49,99 € et 119,99 € (probable prix barré) **[extrait moteur, non vérifié]**. Les autres prix : **[N.D.]**.

**Dédoublonnage appliqué :** renuevo.de (2 pages) = 1 marque ; Stimulicat + Cat Insider + Fera Pets + SerenoSole = flux Stimulicat ; Cosylane/Elaya = 1 marque.

### 4.2 B2 — Même format, positionnement lit/déco (catalogues, marketplaces)
| Acteur | Domaine / canal | Produit | Signal |
|---|---|---|---|
| Aussie Pet | aussie-pet.com | `handwoven-cotton-rope-cat-bed` (annonces catalogue sans rapport avec le produit) | 239 annonces actives, 46 766 visites/mois **[ESTIM. OUTIL]** |
| NioPets | niopets.com | `handwoven-cotton-rope-cat-bed` | Annonces 2024–2025, arrêtées |
| Joypolly | joypolly.com | « Hemp & Cotton Rope Nest » | IE/NL/US, avr.–sept. 2026, 9 actives (tous produits) |
| CutyPet | cutypet.com | « woven cat basket » | GB/US, sept.–oct. 2025 |
| Brownstick | brownstick.com | « hand-woven natural cozy cat bed » | nov. 2025 |
| British Pets | britishpets.uk | « hand-woven rattan cat scratching bed » | GB, actif (annonces catalogue) |
| UAMLY (zooplus.fr) | zooplus.fr | Panier corde tressée 40×40×14 cm, balle, pliable | Distributeur majeur — prix **[N.D.]** |
| Kahume (Amazon.de) | amazon.de | Panier en cordes de coton lavable | 19,90 € **[extrait moteur]** |
| Listings « Instinct Basket / Stimulicat » | amazon.com, walmart.com, ebay.com | Paniers corde coton + coussin + balle | 17–24 $ **[extraits moteur]** |
| AliExpress | aliexpress.us | « Cat Instinct Basket » corde de coton tressée | à partir de 7,6 $ en promotion, hors livraison **[extrait moteur]** |

### 4.3 C — Alternatives au même besoin
Lits-griffoirs en carton (« Kratzkokon », Alp CH / pelzfreunde.com, DE/CH, 2025) ; lits-griffoirs ovales en sisal (Candyoou, NL, août 2026 ; Moonbeamt, IE) ; griffoirs ronds avec balle (Maison Liora, Theraniss, FR, 2026) ; arbres à chat (Maiscasa.pt, CY Deals, Mesmo Bom) ; diffuseurs de phéromones (Feliway FR/UK — très forte diffusion, angle « stress/griffades ») ; coupe-griffes.

### 4.4 D — Hors sujet (exclus du classement)
« Boutiques similaires » TrendTrack (toutes des boutiques de harnais : Roamora, Pantania, Domus Animal, Pewna Łapka, AdoraPaws, SurferCat, Cat Harness Australia, CATFIT, GAT Original, felinde…).

---

## 5. Publicités et voix du client

### 5.1 Sélection de créations (hook = transcription TrendTrack ; vidéos non visionnées)
| # | Marque | ID annonce | Pays princ. | Format | 1re vue → dernière vue | Statut | Portée UE | Δ 7 j / 30 j | Hook (source) |
|---|---|---|---|---|---|---|---|---|---|
| 1 | Stimulicat | 1685286859235052 (collation 1041624258462083) | IT | vidéo | 31/07 → 15/08/2026 (collation active, verdict « improving ») | active | 986 035 | — | « This is what would happen to a cat whose owner ignores her scratching need. » (transcription) |
| 2 | Stimulicat | 1842576809768760 | PL | vidéo | 20/04 → 29/05/2026 | « active » (vue ancienne) | 748 486 | — | idem #1 (variante) |
| 3 | Stimulicat | 1724938698812379 | IT | vidéo | 04/07 → 06/10/2026 | active | 593 290 | — | idem #1 |
| 4 | Stimulicat | 1902998823753032 | IT | vidéo | 06/05 → 25/05/2026 | active* | 490 164 | — | « Most owners never find out what slowly happens to a cat whose scratching need has been ignored… » |
| 5 | Stimulicat | 2019122852039297 | IT | vidéo | 24/07 → 28/07/2026 | active* | 464 756 | — | « This is what could happen to your cats if they all use the instinct basket every day for two weeks. » |
| 6 | Stimulicat | 1583627913440583 | IT | vidéo | 24/08 → 16/09/2026 | active* | 464 485 | — | « Here's a cat hack to stop your cat from scratching your furniture forever. » |
| 7 | Stimulicat | 4488637938076779 | NL | vidéo | 06/07 → 13/07/2026 | active* | 461 462 | — | « Indoor cats need their nails clipped every two weeks, for life. » |
| 8 | Stimulicat | 988127326967114 | IT | vidéo | 06/05 → 23/05/2026 | active* | 445 760 | — | « How does a cat ask for help when she is in pain? » |
| 9 | Stimulicat | 1349625957217188 | IT | vidéo | 07/04 → 18/04/2026 | active* | 305 992 | — | « Making biscuits isn't a quirk. » |
| 10 | Stimulicat | 2101136440571906 | NL | vidéo | 04/09 → 09/09/2026 | active* | 273 833 | — | « This is what a cat's claw looks like when it sinks into the right scratching surface. » |
| 11 | Stimulicat | 1527444395437725 | IT | vidéo | 26/05 → 29/05/2026 | active* | 211 826 | — | « After 15 years with my cat, here are three things I'll never do again. » |
| 12 | Stimulicat | 985025447384396 | FR | vidéo | 07/04 → 17/04/2026 | active* | 201 481 | 0 | « Outdoor cats never need their nails clipped. » (+ « Vets who see this every week… ») |
| 13 | Stimulicat | 1466146931989257 (coll. 1001091596275726) | IT | vidéo (chanson) | 04/09 → 06/10/2026 | active | 190 772 | +9 391 / +153 717 | « They say a loyal friend is true » (paroles chantées) ; copie : « Do not buy the Instinct Basket if you love your cat. » |
| 14 | Stimulicat | 1417965509787687 | IT | vidéo | 13/02 → 12/03/2026 | active* | 148 867 | — | « They warned us this day might come… We're going out of business! » |
| 15 | Stimulicat | 1013530704444914 | IT | vidéo (chanson POV) | 15/05 → 25/05/2026 | active* | 145 482 | — | « I'm the nail on your cat's front paw… » |
| 16 | Stimulicat | 1080877764584385 (coll. 1405875501065526) | NL | vidéo UGC | 30/09 → 06/10/2026 | inactive | 29 372 | +29 285 | « Do not buy the instinct basket if you're not ready to lose her to it. » |
| 17 | Stimulicat | 976947721328262 | NL | image | 29/09 → 06/10/2026 | active | 46 197 | +39 229 | Copie : « Not one to gatekeep so here you go 😼 ✔ $159.95 down to $79.95 tonight only » (pas de transcription) |
| 18 | Nidora (Junga) | 4325456347765347 | ES | vidéo | 12/09 → 05/10/2026 | active | 491 582 | +30 901 / +350 482 | « Esto es lo que le pasa a un gato cuyo dueño ignora su necesidad de rascar. » (traduction de #1) |
| 19 | Nidora (Junga) | 1585506846108719 | ES | vidéo | 27/09 → 05/10/2026 | active | 174 408 | +159 404 | « Esto es lo que le pasa a la uña de un gato cuando por fin encuentra la superficie correcta. » (traduction de #10) |
| 20 | Fellnest (Mindful.Insider) | 1394015419499156 | DE | vidéo | 31/08 → 03/10/2026 | inactive | 201 232 | +4 980 / +147 406 | « Das hier würde mit einer Katze passieren, deren Kratzbedürfnis ignoriert wird. » |
| 21 | Panier Amara (Furanza) | 1413585197351845 | FR | vidéo | 20/08 → 11/09/2026 | inactive | 32 966 | — | « Nous présentons nos excuses à tous ceux qui ont acheté le panier Amara parce qu'on vous a menti. » |
| 22 | Aristocatto | 1885111282654841 | IT | vidéo | 02/10 → 05/10/2026 | active | 15 768 | +15 648 | **[N.D.]** (transcription non extraite) |

\* « active » selon TrendTrack malgré une dernière vue ancienne : **ne pas interpréter comme une performance actuelle**.

Liens : bibliothèque Meta `https://www.facebook.com/ads/library/?id=<ID>` (construit à partir d'identifiants réels, non ouvert) ; médias TrendTrack `medias.trendtrack.io/...` (résolus, non ouverts — CDN bloqué). Voir annexe B pour les URL complètes.

### 5.2 Familles d'angles et concepts
| Famille | Concepts (ex.) | Ouverture | Mécanisme | Preuve revendiquée | Offre / CTA |
|---|---|---|---|---|---|
| **A. Douleur cachée / ongles** (dominante : 13 des 20 annonces les plus diffusées, 5,30 M sur 7,19 M de portée cumulée, soit ≈ 74 %) | #1–4, #7–9, #12, #15 | Chronologie « mois 1, 2, 3 », « signes qu'elle souffre » | Écorce → griffes limées ; phéromones | « Research shows », « vets » | Garantie 45 j, −50 %, 20 000+ vendus |
| **B. Adoption / « ne l'achetez pas si… »** | #13, #16, Amara | Anti-pub ironique | Le chat « s'approprie » le panier | Témoignage de propriétaire | Coussin offert, rupture imminente |
| **C. Multi-chats / timeline 2 semaines** | #5 | « Voici ce qui arrivera en 2 semaines » | Odeur qui s'accumule | Progression jour par jour | Garantie |
| **D. Canapé / hack** | #6 | « Cat hack » | Le chat cherche une surface qui « résiste » | Récit personnel | — |
| **E. Urgence / fermeture** | #14 | « We're going out of business » | Matière bientôt indisponible | — | Dernier stock |
| **F. Promo statique** | #17 | « Not one to gatekeep » | — | — | Prix barré « tonight only » |

**Changement de hook vs nouveau concept :** #1, #2, #3, #4, #18, #20 = **même script** avec ouvertures/langues différentes ; #9, #13, #15 = nouveaux concepts (« biscuits », chanson, POV de la griffe).

### 5.3 Voix du client (extraits rapportés par moteur de recherche — pages non ouvertes, traduction signalée)
| Verbatim (traduction FR) | Source | Tonalité |
|---|---|---|
| « Une de mes chattes l'adore pour griffer et dormir, elle a sauté dedans dès l'ouverture du colis. » | Loox Stimulicat (résumé moteur) | + |
| « Mieux que n'importe quel griffoir que j'ai acheté, esthétiquement et fonctionnellement. » | Loox (résumé moteur) | + |
| « Un chat de refuge anxieux l'utilise 20 heures par jour comme refuge. » | Avis (résumé moteur) | + |
| « Sur 11 chats, 8 l'ont adopté tout de suite, 2 n'ont montré aucun intérêt. » | Avis (résumé moteur) | mitigé |
| « Le coussin sent mauvais » ; « colis petit et très compressé » | Trustpilot (résumé moteur) | − |
| « Il ne s'en approche même pas. » | Trustpilot (résumé moteur) | − |
| « L'une l'adore, l'autre n'y est jamais allée. » | Trustpilot (résumé moteur) | mitigé |
| « Vraiment déformé, il ne reprend pas sa forme. » | Avis Amazon paniers corde (résumé moteur) | − |
| « Frais de retour très élevés », « livraison internationale longue » | Trustpilot (résumé moteur) | − |

**Lecture (non représentative, échantillon non défini) :** déclencheurs = canapé abîmé, griffoirs ignorés, envie d'un coin douillet ; objections = adoption incertaine (surtout multi-chats), odeur/forme à réception, prix vs marketplace, coût des retours, délais.

### 5.4 Allégations sensibles (bien-être animal)
- « Lime les griffes / plus besoin de couper » : contredit par les recommandations de refuges et marques (le griffage retire les couches mortes ; la coupe régulière reste nécessaire chez les chats d'intérieur — SF SPCA, Purina AU, PetCircle).
- « Absorbe les phéromones de façon permanente » : **aucune preuve sur le produit fini** trouvée.
- « Recommandé par les vétérinaires », « research-backed » : **aucune étude** identifiée.
→ À **ne pas reprendre**.

---

## 6. Comparaison des marchés

### 6.1 Tableau par pays (méthode homogène F1 + F2, voir §1.3)
| Pays | Clones B1 trouvés (actifs) | Plus fort signal concurrent | Diffusion UE Stimulicat (pays principal) | Chats (FEDIAF) | CPM Meta indicatif* | Paiement / contraintes | Couverture |
|---|---|---|---|---|---|---|---|
| **Espagne** | 3 (2) | Nidora : 1,14 M portée, +390 k / 7 j | 9 ann. / 192 k | N.D. | ~6,65 $ | Cartes 62 % ; Bizum | Bonne |
| **Allemagne (+AT)** | 3 (2) | Fellnest : ~360 k, actif depuis juillet | 2 / 230 k | 15,7 M | ~9,05 $ | Exigences légales/confiance élevées | Bonne |
| **France (+BE)** | ≥ 11 (3, tous < 1 sem.) | Amara 107 k (arrêté) ; SoftPawsCo actif | 1 / 201 k | 14,9 M | ~6,95 $ | BE : Bancontact | Bonne |
| **Pays-Bas (+BE)** | 4 (1) | Elvori : 136 k, +32 k / 7 j | **41 / 2,04 M** | 3,0 M | ~8,58 $ | iDEAL ≈ 70 % | Moyenne |
| **Italie** | 3 (2, < 2 sem.) | Aristocatto : 83 k, +66 k / 7 j | **25 / 5,31 M** | 10,24 M | ~6,06 $ | Portefeuilles ≈ 35 % (PayPal, PostePay), cartes 31–33 %, contre-remboursement ≈ 4 % | Moyenne |
| **Pologne** | 1 (0) | naevi.pl : 5,6 k (test arrêté) | 1 / 748 k | N.D. | ~5,55 $ | BLIK indispensable | Moyenne |
| **Suède** | 1 (0) | Sensicat : 373 (arrêté) | 1 / 30 k | N.D. | N.D. | N.D. | Faible |
| **Royaume-Uni / Irlande** | 3 (1 hors UE probable) | WizzFit (arrêté) ; Stimulicat en anglais | IE 3 / 5 k | 11,4 M (UK) | N.D. | Hors UE (UK) : douane | Moyenne |
| **Portugal** | 0 | — | 2 / 6 k | N.D. | N.D. | N.D. | Faible |
| **Danemark** | 0 | — | — | N.D. | N.D. | N.D. | Faible |
| **Tchéquie** | 0 | — | — | N.D. | N.D. | N.D. | Faible |
| **Hongrie** | 0 | — | 7 / 466 k | N.D. | N.D. | N.D. | Faible |
| **Roumanie** | 0 | — | 2 / 19 k | N.D. | N.D. | N.D. | Faible |
| **Grèce** | 0 | — | 4 / 160 k | N.D. | N.D. | N.D. | Faible |
| **US (référence)** | Stimulicat + Auravos/Cuddlecom (EN) + marketplaces | Stimulicat (93,9 % de son trafic) | — | — | — | Ancrage prix Amazon/Walmart 17–24 $ | Moyenne |

\* CPM : valeurs agrégées citées par des benchmarks tiers (Lebesgue, Adligator… via moteur de recherche, pages non ouvertes) — **ordre de grandeur, non vérifié**.

### 6.2 Réponse 1 — Où observe-t-on le moins de concurrence directe ?
**Portugal, Danemark, Tchéquie, Hongrie, Roumanie, Grèce** : aucun clone localisé trouvé avec deux familles de requêtes. Puis **Pologne** (un test de 7 annonces, arrêté le 02/10/2026). **Attention :** « aucun concurrent retrouvé » ≠ « aucune concurrence » (les déclinaisons grammaticales peuvent échapper à la recherche par mots) et ≠ « marché validé » (la demande n'y est pas démontrée, hors diffusion anglophone de Stimulicat en Hongrie et en Grèce).

### 6.3 Réponse 2 — Quel marché pour un premier test commercial ?
**Recommandation : Italie** (confiance moyenne-faible).
- **Pour :** (a) la diffusion UE de Stimulicat se concentre en Italie (54 % de sa portée, 25 annonces, d'avril à octobre 2026) alors qu'il n'y propose aucune création en italien — signal indirect de demande et de rentabilité *probable* pour lui, puisqu'il continue à investir [HYPOTHÈSE] ; (b) 10,24 M de chats ; (c) CPM indicatif modéré ; (d) concurrents locaux très récents (Aristocatto 23/09, Felyra 03/10) — le marché n'est pas encore figé ; (e) paiements standards (PayPal, cartes) faciles à mettre en place.
- **Contre :** 2 clones actifs en accélération ; localisation italienne (créas, SAV) à produire ; la portée ne prouve pas les ventes.
- **Pourquoi pas le pays le moins concurrentiel ?** Ces marchés sont petits (PT, DK, GR, CZ, RO) ou sans preuve de demande (HU), et souvent à paiements/langues spécifiques ; la Pologne reste une alternative sérieuse.

**Alternative 1 : Pologne** — un seul test concurrent arrêté, CPM le plus bas de l'échantillon, Stimulicat y a obtenu 748 k de portée avec une seule annonce anglaise ; mais pouvoir d'achat et prix plafond plus bas, BLIK indispensable, signal de demande ponctuel (pas de diffusion continue).
**Alternative 2 : Allemagne** — plus grande population féline d'Europe, un seul clone établi (Fellnest), mais CPM le plus élevé et exigences de conformité/confiance plus fortes (mentions légales, droit de rétractation, allégations).
**À éviter pour ce premier test :** Espagne, Pays-Bas, France, US/UK (raisons au §0).

**Ce qui changerait la décision :** coût rendu réel du produit (> 25 €) ; lancement par Stimulicat de créations en italien ; accélération continue d'Aristocatto/Felyra sur 2 semaines ; délais de livraison > 10 jours vers l'Italie ; un test pilote en Pologne nettement meilleur.

---

## 7. Positionnement, offre et plan de test

### 7.1 Trois positionnements
| | P1 — « Le griffoir qu'il adopte vraiment » (**recommandé**) | P2 — « Le coin à lui, beau dans le salon » | P3 — « Un territoire par chat » (multi-chats) |
|---|---|---|---|
| Persona | Propriétaire de chat d'intérieur, appartement, canapé abîmé, déjà déçu par des griffoirs | Propriétaire attentif à la déco, cache les objets pour chat | Foyer de 2–3 chats, tensions/partage |
| Situation déclencheuse | Nouveau canapé, déménagement, griffoir ignoré | Arrivée d'invités, refonte déco | Arrivée d'un nouveau chat |
| Bénéfice démontrable | Le chat griffe le bord et dort dedans (vidéo brute) | Objet esthétique : lit + griffoir + cachette | Chaque chat a son panier |
| Différenciation | Honnêteté : pas de promesse « plus jamais de coupe », adoption filmée non coupée, garantie d'adoption | Matière naturelle, coloris, photos intérieur | Bundle 2 paniers |
| Preuves nécessaires | Vidéos UGC réelles de 48 h ; taux d'adoption mesuré sur un panel de testeurs | Photos clients en intérieur | Vidéos multi-chats |
| Objections | « Il ignore tout », odeur/forme à réception, prix vs Amazon | Durabilité, poils | « Le 2e chat n'y va pas » |

**Contraste assumé :** tous les clones répètent « ongles douloureux / écorce / phéromones ». P1 prend le contre-pied : *on vous montre ce qui se passe vraiment, sans promesse médicale*.

### 7.2 Offre (prix = hypothèses tant que les coûts ne sont pas connus)
- **Offre principale :** Panier + coussin amovible lavable + balle — **49,90 € TTC livraison incluse** (repères : Nidora 49,99 € vu via moteur ; Stimulicat 79,95 $). Garantie d'adoption 30 jours (en plus du droit légal de rétractation de 14 jours) avec **retour simplifié** (réponse aux plaintes Trustpilot).
- **Bundle :** 2 paniers (multi-chats) **84,90 €**.
- **Complément :** housse/coussin de rechange **14,90 €** (lavage) ; option herbe à chat séchée (à sourcer, sans allégation).
- **À proscrire :** prix barré fictif, compte à rebours permanent, « fermeture », faux avis/experts.

### 7.3 Économie de commande (scénarios HYPOTHÉTIQUES)
Base : prix TTC 49,90 € ; TVA Italie 22 % (applicable après le seuil OSS de 10 000 € de ventes à distance UE) → revenu HT 40,90 €. Frais de paiement supposés 2,5 % du TTC + 0,25 € = 1,50 €.

| Poste (par commande) | Optimiste | Central | Pessimiste |
|---|---|---|---|
| Revenu net HT | 40,90 € | 40,90 € | 40,90 € |
| Produit + préparation + livraison (coût rendu supposé) | −14,00 € | −20,00 € | −26,00 € |
| Paiement | −1,50 € | −1,50 € | −1,50 € |
| Provision retours/SAV (% du HT) | −2,05 € (5 %) | −3,27 € (8 %) | −4,09 € (10 %) |
| **Contribution avant publicité = CPA d'équilibre** | **23,35 €** | **16,13 €** | **9,31 €** |
| ROAS d'équilibre (base CA TTC, comme affiché par Meta) | 2,14 | 3,09 | 5,36 |
| ROAS d'équilibre (base CA HT) | 1,75 | 2,54 | 4,39 |

Bundle 2 paniers à 84,90 € TTC (HT 69,59 €), scénario central : coût 40 €, paiement 2,37 €, retours 8 % = 5,57 € → **contribution 21,65 €** ; ROAS d'équilibre TTC 3,92.
**Aucune valeur de réachat n'est intégrée.** Les coûts sont des hypothèses : le prix public AliExpress (≈ 7,6 $ en promo, hors livraison) ne constitue pas un coût fournisseur confirmé.

### 7.4 Plan de test (Italie)
**Phase 0 — Validation produit hors publicité (avant toute dépense pub)**
- Commander 2–3 échantillons chez 2 fournisseurs ; vérifier matière réelle (coton ? jute ?), odeur, tenue de forme après dépliage, tailles M/L, délai réel vers l'Italie.
- Tourner ses propres vidéos d'adoption avec de vrais chats (5–10 foyers testeurs), sans coupe ni mise en scène.

**Phase 1 — Validation créative (7–10 jours)** : campagne Ventes, Italie, 3 angles × 2 hooks = 6 vidéos, page produit directe.
Scénarios de budget (**non autorisés, à décider par vous**) : S1 30 €/j (≈ 210–300 €), S2 60 €/j (≈ 420–600 €), S3 100 €/j (≈ 700–1 000 €).

| Angle | Hook 1 (FR / IT) | Hook 2 (FR / IT) |
|---|---|---|
| A. Adoption sans promesse | « Trois griffoirs ignorés. Celui-ci, elle l'a pris en 48 h — voici les images brutes. » / « Tre tiragraffi ignorati. Questo l'ha preso in 48 ore: ecco il video senza tagli. » | « Avant de racheter un griffoir, regarde où ton chat griffe vraiment. » / « Prima di comprare un altro tiragraffi, guarda dove graffia davvero il tuo gatto. » |
| B. Déco | « Le seul objet pour chat que j'ai laissé au salon quand les invités sont arrivés. » / « L'unica cosa per il gatto che ho lasciato in salotto quando sono arrivati gli ospiti. » | « Lit, griffoir, cachette : un seul panier tressé au lieu de trois objets en plastique. » / « Cuccia, tiragraffi e rifugio: un solo cesto intrecciato al posto di tre oggetti di plastica. » |
| C. Multi-chats | « Deux chats, un panier : test honnête sur 7 jours. » / « Due gatti, un cesto: test onesto di 7 giorni. » | « Pourquoi le 2e chat n'y est entré qu'au jour 4 (et ce qu'on a changé). » / « Perché il secondo gatto ci è entrato solo al giorno 4 (e cosa abbiamo cambiato). » |

**Phase 2 — Validation de l'offre et de la page** : page produit vs page éditoriale (« Perché il tuo gatto ignora i tiragraffi ») ; unité vs bundle 2 paniers.

**Indicateurs et règles de décision (liés au scénario central, CPA d'équilibre ≈ 16 €) :**
| Niveau | Indicateur | Règle (heuristique, à ajuster à vos coûts réels) |
|---|---|---|
| Créa | Taux d'accroche 3 s, CTR lien, CPC | Couper une créa après ≈ 2× CPA d'équilibre dépensé (≈ 32 €) sans ajout au panier |
| Créa/produit | Coût par ajout au panier, CPA | Couper après ≈ 3× CPA d'équilibre (≈ 48 €) sans achat ; garder si CPA ≤ CPA d'équilibre sur ≥ 3 achats |
| Produit | Achats sur ≥ 2 angles différents | Produit « validé » si ≥ 2 angles atteignent CPA ≤ équilibre ; sinon arrêter (pas de seuil universel) |
| Offre | Panier moyen, part de bundles, taux de retour | Bundle conservé s'il augmente la contribution par commande sans dégrader le taux de conversion |
| Échelle | CPA stable 3 jours | Hausse de budget progressive (+20–30 %/48 h) |

### 7.5 Trame vidéo build in public (5 parties)
1. **Découverte** — « J'ai trouvé un panier pour chat qui fait ~2 M d'impressions par mois en Europe… en anglais uniquement » (chiffre TrendTrack daté, à montrer à l'écran).
2. **Preuves** — copies Amazon à 17–24 $, ≥ 30 clones en 4 mois, Nidora qui accélère en Espagne (données datées, sources visibles).
3. **Objections** — allégations douteuses, risques (Omnibus, retours), estimation de ventes incohérente de l'outil.
4. **Décision** — Italie, positionnement honnête, budget de test choisi et affiché.
5. **Prochain test** — échantillons reçus, première vidéo d'adoption réelle, résultats réels publiés (même mauvais). Aucune promesse de gain.

---

## Annexe A — Références (chiffres et règles)
- Recommandations de coupe des griffes : [SF SPCA – Cat Claw Clipping](https://www.sfspca.org/resource/claw-clipping/) ; [Purina AU – How to cut a cat's claws](https://www.purina.com.au/guide-to-cutting-cat-claws.html) ; [PetCircle](https://www.petcircle.com.au/discover/how-to-trim-cat-nails).
- Directive Omnibus / prix de référence 30 jours : [RPC – guidance Commission](https://rpclegal.com/snapshots/consumer/spring-2022/european-commission-publishes-guidance-on-price-promotions-under-the-omnibus-directive) ; [idnovate – art. 6a](https://www.idnovate.com/public/idn-omnibus/omnibus-landing-en.html).
- TVA OSS (seuil 10 000 €) : [Hellotax – VAT threshold Italy](https://hellotax.com/blog/vat-threshold-in-italy/) ; [RSM Italy – e-commerce VAT](https://www.rsm.global/italy/rsmsts/en/news/e-commerce-new-vat-regime-entities-who-make-online-sales-final-consumers-other-countries-eu-one) ; [Stripe – VAT in Italy](https://stripe.com/resources/more/value-added-tax-for-freelancers-italy).
- Population féline (FEDIAF 2025) : [FEDIAF – Facts & Figures 2025](https://europeanpetfood.org/_/news/fediaf-publishes-2025-facts-and-figures/) ; [The Animal Economics – synthèse](https://theanimaleconomics.com/fediaf-statistics-europe-is-home-to-581-million-pets.html) ; [Flamingo – pets in Europe](https://www.flamingo.be/en/news/pets-in-europe-trends-and-statistics).
- Paiements : [Cross-Border Magazine – Italy 2025](https://cross-border-magazine.com/e‑commerce-payment-italy-2025/) ; [Stripe – Italy](https://stripe.com/gb/resources/more/online-payment-methods-italy/) ; [Cross-Border – Netherlands 2025](https://cross-border-magazine.com/e‑commerce-payment-landscape-netherlands-2025/) ; [BLIK – 2025](https://www.blik.com/en/nearly-3-bn-blik-transactions-in-2025-and-over-2-m-new-users) ; [Stripe – Bizum](https://stripe.com/resources/more/bizum-for-buisinesses-spain) ; [Landmark – Belgian e-commerce](https://landmarkglobal.com/eu/en/news-insights/top-10-essential-facts-about-belgian-e-commerce-2025-edition/).
- CPM indicatifs : [Lebesgue – CPM by country](https://lebesgue.io/facebook-ads/facebook-cpm-by-country) ; [Adligator – Meta CPM by country 2026](https://adligator.com/blog/meta-ads-cpm-by-country-benchmarks).
- Avis : [Trustpilot Stimulicat](https://www.trustpilot.com/review/www.stimulicat.com) ; [Loox Stimulicat](https://loox.io/s/uz0V-Mpwgm) ; [Walmart – avis panier « Stimulicat »](https://www.walmart.com/reviews/product/20255864125).
- Prix marketplace/fournisseur : [Amazon – Instinct Basket listing](https://www.amazon.com/Instinct-Basket-Stimuli-Handwoven-Cushion/dp/B0H9B1G5H6) ; [Walmart – listing](https://www.walmart.com/ip/Instinct-Basket-Stimulicat-Cat-Bed-Stimulicat-Cat-Bed-Rope-Cotton-Cushion-Eliminates-Bed-Rejection-Round-Pet-Basket-Boho-Catbed-Cats-Handwoven-Scratc/19376359468) ; [AliExpress – cotton rope cat bed](https://www.aliexpress.us/w/wholesale-cotton-rope-cat-bed.html) ; [Amazon.de – Kahume](https://www.amazon.de/Katzenbett-Baumwollseilen-Katzenk%C3%B6rbchen-Schlafplatz-Haustierbett/dp/B09P3YXFJJ) ; [zooplus.fr – UAMLY](https://www.zooplus.fr/shop/chats/paniers_lits_couvertures_chat/couchage/9980050350) ; [Vittasa – Nidora](https://vittasa.com/products/nidora%E2%84%A2-el-territorio-natural-tejido-a-mano-para-tu-gato-de-interior).

Toutes ces pages : **lien résolu via moteur de recherche, page non ouverte** (réseau bloqué).

## Annexe B — Répertoire des liens

Statuts : **[R]** lien résolu (issu d'une source, non ouvert) · **[C]** URL construite à partir d'un identifiant réel et d'une route connue, non ouverte · **[X]** accès impossible depuis cet environnement · **[NR]** non retrouvé. Les liens TrendTrack exigent votre compte (workspace `w-s-workspace-BG9HrBQ`). Bibliothèque Meta : `https://www.facebook.com/ads/library/?active_status=all&ad_type=all&country=ALL&view_all_page_id=<PAGE>` [C].

### Référence
| Élément | Lien | Statut |
|---|---|---|
| Site | https://www.stimulicat.com | [R][X] |
| Fiche produit | https://www.stimulicat.com/products/instinct-basket-meet-the-first-research-backed-natural-territory-for-indoor-cats | [R][X] |
| Landing principale | https://try.stimulicat.com/wants-to-prevent-nail-pain-feature-benefit-territory-basket-79-95-offer | [R][X] |
| Landing secondaire | https://try.stimulicat.com/copy-of-wants-to-be-good-cat-parent-feature-benefit-territory-basket | [R][X] |
| Advertorial (Shopify) | https://www.stimulicat.com/pages/advertorial-page-sep-18-13-38-01 | [R][X] |
| Instinct Mat | https://www.stimulicat.com/collections/best-sellers/products/instinct-mat-the-scratching-mat-her-biology-actually-recognizes | [R][X] |
| TrendTrack boutique | https://app.trendtrack.io/en/w-s-workspace-BG9HrBQ/shops/81116494-e148-4241-8e2e-cf93b67381d4 | fourni par vous |
| TrendTrack try.stimulicat.com | https://app.trendtrack.io/en/w-s-workspace-BG9HrBQ/shops/e24624ef-d592-47ea-b6cd-06c17d5002db | [C] |
| Bibliothèque Meta – Stimulicat | page 711004312088223 | [C] |
| Bibliothèque Meta – Cat Insider | page 756628667526995 | [C] |
| Annonce #1 (bibliothèque) | https://www.facebook.com/ads/library/?view_all_page_id=711004312088223&id=2409191246282961 | [R] (TrendTrack) |
| Annonce #13 | https://www.facebook.com/ads/library/?view_all_page_id=711004312088223&id=1466146931989257 | [R] (TrendTrack) |
| Annonce #16 | https://www.facebook.com/ads/library/?view_all_page_id=711004312088223&id=1661848542237145 | [R] (TrendTrack) |
| Vidéo #1 | https://medias.trendtrack.io/facebook/video/a443fc6d2e07a437aa32344a7431c1ca96e4ec80a5152361d3bcf09ded7c6054.mp4 | [R][X] |
| Vidéo #13 | https://medias.trendtrack.io/facebook/video/6004112253b92c40f033ac7a9ecc6aa3541a49435a6bc29f3d1c6312fa162988.mp4 | [R][X] |
| Vidéo #16 | https://medias.trendtrack.io/facebook/video/7bc2d7cd3aed3eafe1ac3bf45c033efea41570d069fe5471e853bc14401a2b5a.mp4 | [R][X] |
| Visuel #17 | https://medias.trendtrack.io/facebook/image/b339ab73e1ca7ff0d3fd4eaaa6b4289750bdc36a60bf351a9dbdd09f575c8de3.jpg | [R][X] |
| Autres annonces Stimulicat | `https://www.facebook.com/ads/library/?id=<ID>` avec les ID du §5.1 | [C] |

### B1 — Clones d'angle
| Marque | Site / landing | TrendTrack | Page Meta (ID) | Annonce représentative |
|---|---|---|---|---|
| Nidora | https://vittasa.com/pages/garras-gato-interior [R] ; fiche : https://vittasa.com/products/nidora%E2%84%A2-el-territorio-natural-tejido-a-mano-para-tu-gato-de-interior [R] | /shops/bdf52d98-f254-4b1d-bf5c-ee45f9e3f272 [C] | 590247237507990 | 4325456347765347, 1585506846108719 [C] |
| Fellnest | https://renuevo.de/pages/preventnailpain_listicle [R] ; https://renuevo.de/pages/fellnest-spdp [R] | /shops/24ffaf78-c2b7-44fe-a76e-5d9539a28f99 [C] | 868687526335524 ; 946488275218209 | 1394015419499156, 1040553688754110 [C] |
| Elvori | https://elvori.nl/pages/elvori-reviews [R] | /shops/91b9e542-cf75-4b8f-92fc-ebb9ed13df80 [C] | 670768856121471 | 2195355674344631 [C] |
| Panier Amara (Furanza) | https://support.get-novera.com/pages/listicle-amara [R] | /shops/6fc529c0-81cd-4cdb-93fe-18a74254b57d [C] | 391140380749947 | 1413585197351845 [C] |
| Aristocatto | https://aristocatto.com/products/gattedrale-rifugio-anti-stress-tiragraffi-letto-natu… (URL tronquée dans la source) [R partiel] | /shops/7eb50d86-5215-4975-8507-690d8dd61e1d [C] | 1291286530740829 | 1885111282654841 [C] |
| SoftPawsCo (Reisena) | https://softpawsco.com/fr-fr/pages/claw-basket-lis [R] | /shops/4c240248-9889-4243-a3ff-9444a4380e76 [C] | 477138132139130 | 1108183301659830 [C] |
| Felyra | https://myfelyra.com/pages/main-presale-cesta [R] | /shops/66700ab6-e75a-4408-84a1-610455def7b7 [C] | 1513181175202693 | 1803935733946635 [C] |
| Comodea | https://comodea-home.com/pages/perche-il-gatto-si-mordicchia-le-unghie [R] | /shops/c03f1378-8689-4acf-8ed6-75817cb3f9f8 [C] | 1266363966550990 | 1085826390472253 [C] |
| Cosalia | https://cosalia-home.com/pages/por-que-tu-gato-se-muerde-las-unas [R] | [NR] | [NR] | 1634822134931745 [C] |
| Zarpa (Silenxio) | https://silenxio.com/products/cesta-rascadora-de-gato [R] | /shops/2eed0952-5f3f-4a1f-89c8-ccd62734b412 [C] | 1258425370698299 | 1077996218323688 [C] |
| Cosylane | https://cosylanehome.com/de/pages/cosycat [R] | /shops/690c417a-d448-45d3-8421-fa485a1d89e2 [C] | 1042326342306473 | 1280614790836602 [C] |
| Elanzo | https://elanzo.nl/products/purrnest [R] | [NR] | 815727681626586 | 995851219728904 [C] |
| Loria | https://trouwepoot.nl/products/instinct-mand-het-eerste-wetenschappelijk-onderbouwde-… (tronquée) [R partiel] | [NR] | 985680704624087 | 2198372691033234 [C] |
| Wooflyx | https://wooflyx.com/pages/de-nagelschmerzen-vorbeugen-vorteil-territorium-korb [R] | [NR] | 1033893756473429 | 1014565247930196 [C] |
| Zevlo | https://le-panier-que-les-chats-raffolent.zevlo.co/ [R] | [NR] | 763815883490348 | 1027766536494414 [C] |
| ÉVEZA | https://xn--veza-9oa.com/pages/prevenir-douleurs-ongles-avantages [R] | /shops/999cb77a-cd20-441c-ad89-1754b0273647 [C] | 1287570251099977 | 1430109109104323 [C] |
| Isba&Co | https://isba-co.com/products/le-panier-instinct-isba-co-le-premier-panier-bien-etre-c… (tronquée) [R partiel] | [NR] | 1188137074386739 | 1053054967705049 [C] |
| Meowlia | https://meowlia.com/products/panier [R] | [NR] | 1067324686466001 | 4643893385935100 [C] |
| Fleecky | https://fleecky.com/pages/prévenir-les-douleurs-aux-griffes [R] | [NR] | 860218714151808 | 2184440152132685 [C] |
| Shop Veralae | https://aveloriae.com/pages/griffes-chat-interieur [R] | [NR] | 1070604682808541 | 2236668970399673 [C] |
| OlyPet | https://olypet.fr/pages/griffes-chat-lis1 [R] | [NR] | 884569114744853 | 1597394968801838 [C] |
| PawFabric (Milky Fabrics) | https://paw-fabric.com/products/panier-griffoir-instinct [R] | /shops/1f711921-5578-4266-98dc-408d7737b3b5 [C] | 1065767929951423 | 2656609501401696 [C] |
| Mon Adorable Félin | https://www.monadorablefelin.com/products/panier-pour-chat-griffoir [R] | /shops/006a6fbd-2667-438f-b18a-3f13da96c5e8 [C] | 105371138534668 | 851783081353460 [C] |
| naevi | https://naevi.pl/pages/gniazdo-instynktu-blog [R] | /shops/4fc91d6d-936d-498f-9b2f-ca987e2cf8da [C] | 1024693717398503 | 1361242442758425 [C] |
| Sensicat | https://shopmonura.com/pages/landingpagesnarkning12 [R] | [NR] | 958263377378310 | 1062493636342488 [C] |
| WizzFit | https://wizzfit.com/products/handwoven-rope-cat-bed [R] | /shops/44aa6d9d-4cf4-4616-94f1-9c523e964357 [C] | 612520731938361 | 1598337121909317 [C] |
| Auravos | https://auravos.store/pages/only-one-she-used [R] | [NR] | 705020839370685 | 1471434628151838 [C] |
| Cuddlecom | http://cuddlecom.com/ [R] | [NR] | 1187966641068146 | 924090123829976 [C] |
| Pet Heaven (CL) | https://www.petheaven.cl/products/cat-nest-su-rincon-para-rascar-descansar-y-sentirse-seguro [R] | [NR] | 1129985643534495 | 1572368320797786 [C] |
| NaturaPurr (MX) | https://naturapurr.com/products/naturapurr [R] | [NR] | 1156443824226330 | 2250318639142498 [C] |

TrendTrack : préfixer `/shops/…` par `https://app.trendtrack.io/en/w-s-workspace-BG9HrBQ`.

### B2 — Même format, positionnement lit/déco
| Acteur | Lien | TrendTrack | Statut |
|---|---|---|---|
| Aussie Pet | https://aussie-pet.com/products/handwoven-cotton-rope-cat-bed | /shops/188e0ebc-3a8f-4f04-86a5-491706fabf7c | [R]/[C] |
| Joypolly | https://joypolly.com/products/handwoven-cotton-rope-cat-bed | /shops/063b97c6-726f-450d-8435-7367ee899b7f | [R]/[C] |
| NioPets | https://niopets.com/products/handwoven-cotton-rope-cat-bed | [NR] | [R] |
| CutyPet | https://cutypet.com/collections/pets | [NR] | [R] |
| Brownstick | https://brownstick.com/products/hand-woven-natural-cozy-eco-friendly-cat-bed | [NR] | [R] |
| British Pets | https://britishpets.uk/products/hand-woven-rattan-cat-scratching-bed | [NR] | [R] |
| UAMLY (zooplus.fr) | https://www.zooplus.fr/shop/chats/paniers_lits_couvertures_chat/couchage/9980050350 | — | [R] |
| Kahume (Amazon.de) | https://www.amazon.de/Katzenbett-Baumwollseilen-Katzenk%C3%B6rbchen-Schlafplatz-Haustierbett/dp/B09P3YXFJJ | — | [R] |
| Listings « Instinct Basket » | Amazon/Walmart/eBay (Annexe A) | — | [R] |

### C — Alternatives
Alp CH (alp-shop.ch/de/products/kratzbett-katze-pappe) ; Candyoou (candyoou.com/products/wear-resistant-sisal-cat-scratcher-bed) ; Moonbeamt (moonbeamt.com/products/wear-resistant-sisal-cat-scratcher-bed) ; Maison Liora (maisonliorastore.com/products/panier-griffoir-rond-pour-chat-avec-jouet-balle) ; Theraniss (theraniss.com/products/panier-griffoir-anti-canape, TrendTrack /shops/1ec57ef7-fbe6-47b2-810e-1823c35da78d) ; Maiscasa.pt ; CY Deals (cydeals.cy) ; Mesmo Bom (mesmobom.com) ; Feliway FR (feliway.fr/pages/feliway-optimum) et UK (feliway.co.uk). Tous [R], non ouverts.

## Annexe C — Données brutes et limites
- Crédits TrendTrack : 20 000 disponibles au départ, **1 222 utilisés**, 18 778 restants (06/10/2026 19 h 35 UTC).
- Les données brutes JSON (annonces, pages, requêtes par langue) ont été conservées dans le répertoire de travail temporaire de la session ; seules les synthèses figurent ici.
- Aucune action d'écriture n'a été effectuée sur les comptes connectés (TrendTrack, Meta, Shopify…) : lecture seule.
