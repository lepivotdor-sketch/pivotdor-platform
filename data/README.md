# data/README.md — Le Pivot d’Or · Mini Mini Formation

## Rôle du dossier `data/`

Le dossier `data/` contient les fichiers de données publiques et internes non sensibles utilisés par le site Le Pivot d’Or / Mini Mini Formation.

Son rôle est de structurer le catalogue, les fiches de formation, les recommandations, les FAQ, le SEO, les bundles, les KPI non sensibles et le jumeau numérique de gestion.

> Règle maîtresse : ce dossier aide à vendre simple, livrer propre, mesurer les chiffres et améliorer chaque année, sans exposer de données sensibles.

---

## Décision officielle

Le dossier `data/` peut contenir des données utiles au pilotage public ou semi-interne, mais il ne doit jamais devenir un espace client, un CRM sensible, une base Stripe privée ou un coffre-fort.

GitHub Pages est public. Tout fichier placé dans ce dépôt peut potentiellement être consulté.

---

## À créer en premier

Pour éviter le chaos, ne crée pas tous les fichiers du dossier `data/` en même temps.

Ordre recommandé :

1. `formations-index.json` — fichier principal du catalogue.
2. `dashboard-formations.json` — pilotage non sensible du tableau de bord.
3. `kpi-definitions.json` — définitions des scores, seuils et KPI.
4. `faq.json` — questions fréquentes générales.
5. `seo.json` — titres SEO, méta-descriptions, slugs et mots-clés.
6. `bundles.json` — packs simples pour augmenter le panier moyen.
7. `recommandations.json` — recommandations Craig.
8. Fichiers de détail par catégorie, seulement quand le catalogue principal est propre.

Règle : tant que `formations-index.json` n’est pas clair, valide et utile, ne multiplie pas les autres fichiers.

---

## Contenu autorisé

Le dossier `data/` peut contenir :

- titres de formations ;
- catégories ;
- prix publics ;
- descriptions courtes ;
- statuts publics ;
- tags ;
- extraits ;
- FAQ générales ;
- liens publics non sensibles ;
- liens Stripe publics de paiement ;
- notes qualité ;
- notes rentabilité ;
- scores priorité ;
- scores prêt à vendre ;
- statuts de publication ;
- statuts de production non sensibles ;
- statuts de mise à jour ;
- dates de création ;
- dates de mise à jour ;
- prochaine date de mise à jour ;
- versions ;
- contenus marketing publics ;
- angles de contenu ;
- objections/réponses générales ;
- KPI agrégés non sensibles ;
- vues agrégées ;
- clics agrégés ;
- ventes attribuées agrégées ;
- formations les plus demandées ;
- recommandations de formations ;
- informations du jumeau numérique non sensibles.

---

## Contenu interdit

Ne jamais placer dans `data/` :

- mots de passe ;
- clés API ;
- clés secrètes Stripe ;
- webhooks secrets ;
- tokens ;
- emails clients ;
- noms de clients ;
- adresses ;
- reçus Stripe individuels ;
- historiques d’achat individuels ;
- données bancaires ;
- données médicales ;
- données financières personnelles ;
- liens privés critiques ;
- accès clients réels ;
- contenu payant complet non protégé ;
- fichiers complets de formation principale ;
- captures contenant des données privées ;
- notes support client identifiables ;
- conversations clients ;
- données personnelles sensibles.

---

## Fichiers recommandés dans `data/`

```txt
/data
├── README.md
├── formations-index.json
├── formations-details-ia.json
├── formations-details-productivite.json
├── formations-details-apprentissage.json
├── formations-details-business.json
├── formations-details-finances.json
├── formations-details-relations.json
├── formations-details-bonheur.json
├── formations-details-sante.json
├── dashboard-formations.json
├── bundles.json
├── faq.json
├── seo.json
├── recommandations.json
├── tags.json
├── statuts.json
├── kpi-definitions.json
├── actions-pivot-integrees.json
└── exemples/
    └── formation-exemple.json
```

---

## Règles de nommage

Tous les fichiers doivent respecter ces règles :

- minuscules seulement ;
- aucun accent ;
- aucun espace ;
- utiliser des tirets `-` ;
- extension claire : `.json` ou `.md` ;
- nom descriptif ;
- pas de doublons ;
- pas de fichier temporaire comme `test-final-vrai.json` ;
- pas de fichier nommé `nouveau.json` ;
- pas de fichier contenant une date inutile si le fichier est permanent.

Exemples corrects :

```txt
formations-index.json
formations-details-ia.json
dashboard-formations.json
kpi-definitions.json
```

Exemples à éviter :

```txt
Formations IA.json
formation final FINAL.json
clients-prives.json
stripe-secret.json
```

---

## Source unique du catalogue

Le fichier principal du catalogue est :

```txt
formations-index.json
```

Il sert à alimenter :

- `index.html` ;
- `formations.html` ;
- `formation.html` ;
- le dashboard caché non sensible ;
- les recommandations Craig ;
- les priorités Adrien ;
- les filtres publics ;
- les exports CSV non sensibles.

Règle : ne pas créer 400 pages HTML manuelles. Utiliser une page dynamique + JSON.

---

## Catégories officielles

Les seules catégories officielles sont :

1. IA
2. Productivité
3. Apprentissage
4. Business
5. Finances
6. Relations
7. Bonheur
8. Santé

Répartition finale visée : 50 formations par catégorie, pour un total de 400 formations.

Au lancement, les priorités sont :

1. IA
2. Productivité
3. Business
4. Finances

---

## Statuts officiels

### Statut de contenu

```txt
idee
a_creer
en_cours
a_relire
prete
publiee
a_ameliorer
archivee
```

### Statut de vente

```txt
pas_configuree
stripe_a_creer
stripe_pret
paiement_teste
vente_active
vente_suspendue
```

### Statut d’accès

```txt
acces_non_pret
acces_a_tester
acces_pret
acces_active_apres_paiement
acces_suspendu
```

### Statut de mise à jour

```txt
a_jour
mise_a_jour_prevue
a_reviser
en_revision
mise_a_jour_completee
archivee
```

---

## Champs critiques d’une formation

Une formation ne doit pas être publiée si un champ critique est vide.

Champs critiques :

```json
{
  "id": "",
  "titre": "",
  "categorie": "",
  "prix": 0,
  "probleme_resolu": "",
  "promesse": "",
  "description_courte": "",
  "statut": "",
  "publication_autorisee": false,
  "visibilite_public": false,
  "stripe_link": "",
  "url_acces_apres_paiement": "",
  "mention_legale": ""
}
```

---

## Tableau des champs critiques

| Champ | Bloque la publication si vide ? | Utilisé par | Rôle |
|---|---:|---|---|
| `id` | Oui | Catalogue, dashboard, recommandations | Identifiant unique de la formation |
| `titre` | Oui | Catalogue, SEO, fiche formation | Titre public de la formation |
| `categorie` | Oui | Filtres, dashboard, SEO | Classement officiel |
| `prix` | Oui | Page formation, Stripe, catalogue | Prix public |
| `probleme_resolu` | Oui | Page vente, SEO, promesse | Clarifie la douleur client |
| `promesse` | Oui | Page vente, conversion | Explique le résultat possible sans garantie |
| `description_courte` | Oui | Catalogue, SEO, carte formation | Résumé rapide |
| `statut` | Oui | Dashboard, publication | État de production |
| `publication_autorisee` | Oui | Catalogue public | Autorise ou bloque l’affichage public |
| `visibilite_public` | Oui | Catalogue public | Détermine si la formation est visible |
| `stripe_link` | Oui pour vendre | Page formation | Lien de paiement public |
| `url_acces_apres_paiement` | Oui pour vendre | Stripe, accès client | Redirection après paiement |
| `mention_legale` | Oui | Page formation, conditions | Vente finale, accès privé, aucun coaching |
| `note_qualite` | Non, mais seuil requis | Dashboard Adrien | Score qualité |
| `note_rentabilite` | Non, mais seuil requis | Dashboard Adrien | Score rentabilité |
| `score_priorite` | Non, mais recommandé | Dashboard, roadmap | Classement stratégique |
| `score_pret_a_vendre` | Non, mais recommandé | Dashboard caché | Feu vert / jaune / rouge |

Règle : si un champ critique obligatoire est vide, la formation reste en brouillon.

---

## Modèle minimal d’une formation

```json
{
  "id": "formation-0001",
  "titre": "Utilise l’IA pour sauver 3 heures par semaine",
  "categorie": "IA",
  "prix": 15,
  "niveau": "debutant",
  "duree_estimee": "30 minutes",
  "format": ["Accès en ligne", "Checklist"],
  "statut": "prete",
  "publication_autorisee": false,
  "visibilite_public": false,
  "probleme_resolu": "Manque de temps et tâches répétitives.",
  "promesse": "Tu obtiens une méthode simple, une checklist et une prochaine action claire.",
  "description_courte": "Une mini-formation pour transformer une tâche répétitive en mini-système IA simple.",
  "stripe_link": "",
  "url_acces_apres_paiement": "merci.html",
  "type_acces": "acces_numerique_prive",
  "telechargement_complet": false,
  "checklist_telechargeable": true,
  "coaching_inclus": false,
  "vente_finale_apres_activation": true,
  "note_qualite": 85,
  "note_rentabilite": 80,
  "score_priorite": 90,
  "score_pret_a_vendre": 0,
  "tags": ["IA", "productivite", "temps"],
  "formations_recommandees": [],
  "mention_legale": "Produit digital autonome. Aucun coaching inclus. Accès numérique privé. Vente finale dès activation. Résultats variables. Formation éducative générale."
}
```

---

## Blocs recommandés par formation

Chaque formation peut inclure ces blocs :

```json
{
  "mise_a_jour": {
    "date_creation": "",
    "date_derniere_mise_a_jour": "",
    "date_prochaine_mise_a_jour": "",
    "frequence": "annuelle",
    "version": "1.0",
    "statut_mise_a_jour": "a_jour",
    "historique_versions": []
  },
  "progression": {
    "progression_activee": true,
    "nombre_etapes": 0,
    "etapes": [],
    "progression_client": 0,
    "checklist_completee": false,
    "prochaine_action": ""
  },
  "jumeau_numerique": {
    "actif": true,
    "resume_interne": "",
    "etat_global": "idee",
    "fiche_publique_url": "",
    "source_contenu_securisee": "",
    "stripe_pret": false,
    "acces_prive_pret": false,
    "contenu_en_ligne": false,
    "checklist_prete": false,
    "mini_kit_marketing_pret": false,
    "a_mettre_a_jour": false,
    "prochaine_action_interne": ""
  },
  "analytics": {
    "vues_page": 0,
    "clics_stripe": 0,
    "ventes_attribuees": 0,
    "taux_conversion": 0,
    "revenu_total_agrege": 0,
    "source_trafic_principale": ""
  },
  "controle_publication": {
    "test_mobile": false,
    "test_paiement": false,
    "test_redirection": false,
    "test_acces": false,
    "test_seo": false,
    "test_mentions_legales": false,
    "test_aucun_contenu_sensible": false
  }
}
```

---

## Score de priorité

Formule recommandée :

```txt
score_priorite =
(note_rentabilite x 0.30) +
(demande_marche x 0.20) +
(urgence_probleme x 0.15) +
(potentiel_viral x 0.15) +
(facilite_production x 0.10) +
(simplicite_vente x 0.05) +
(lien_prioritaire x 0.05)
```

Interprétation :

- 90 à 100 : priorité immédiate ;
- 80 à 89 : priorité haute ;
- 70 à 79 : à créer bientôt ;
- 60 à 69 : à améliorer avant création ;
- moins de 60 : ne pas créer maintenant.

---

## Score prêt à vendre

Le score `score_pret_a_vendre` doit indiquer si une formation peut réellement être vendue.

Critères :

- qualité ;
- rentabilité ;
- Stripe prêt ;
- page après paiement prête ;
- accès prêt ;
- checklist prête ;
- support prêt ;
- mentions légales visibles ;
- aucun contenu sensible exposé.

Interprétation :

```txt
85 à 100 = Vert : presque prêt ou prêt à vendre
65 à 84  = Jaune : amélioration nécessaire
0 à 64   = Rouge : bloquant
```

---

## Critères de publication

Une formation est publiable seulement si :

- le titre est clair ;
- le problème est précis ;
- la promesse est réaliste ;
- le prix est défini ;
- la formation est prête ;
- la checklist est prête ;
- la FAQ est présente ;
- le lien Stripe fonctionne ;
- la redirection après paiement fonctionne ;
- l’accès privé est testé ;
- le support est prêt ;
- l’affichage mobile est testé ;
- la mention vente finale est visible ;
- la mention aucun coaching est visible ;
- la mention accès numérique privé est visible ;
- la note qualité est au moins 80 ;
- la note rentabilité est au moins 70 ;
- `publication_autorisee` vaut `true` ;
- `visibilite_public` vaut `true` ;
- aucun contenu sensible n’est exposé.

---

## Tests obligatoires avant publication

Chaque formation doit passer les 5 tests suivants :

1. Test client : le client comprend rapidement ce qu’il achète.
2. Test action : la formation fait passer à l’action.
3. Test paiement : le paiement fonctionne.
4. Test accès : l’accès après achat fonctionne.
5. Test sécurité : rien de sensible n’est exposé publiquement.

---

## Règles Stripe dans `data/`

Autorisé :

- lien Stripe public de paiement ;
- nom public du produit ;
- prix public ;
- statut Stripe non sensible ;
- redirection publique après paiement.

Interdit :

- clé secrète Stripe ;
- webhook secret ;
- données de carte ;
- reçu individuel ;
- email client ;
- historique d’achat individuel.

---

## Règles de l’accès privé

Le dossier `data/` peut contenir un statut d’accès, mais pas un vrai accès privé.

Correct :

```json
{
  "statut_acces": "acces_a_tester",
  "type_acces": "acces_numerique_prive",
  "url_acces_apres_paiement": "merci.html"
}
```

Incorrect :

```json
{
  "email_client": "client@example.com",
  "lien_prive_secret": "https://...",
  "mot_de_passe": "..."
}
```

---

## Jumeau numérique interne

Le jumeau numérique est une représentation de gestion, pas une copie du produit payé.

Il peut contenir :

- ID ;
- titre ;
- catégorie ;
- prix ;
- statut ;
- visibilité ;
- score priorité ;
- note qualité ;
- note rentabilité ;
- score prêt à vendre ;
- ventes agrégées ;
- vues agrégées ;
- clics agrégés ;
- prochaine mise à jour ;
- prochaine action ;
- état Stripe ;
- état accès ;
- état checklist ;
- état mini-kit marketing.

Il ne doit pas contenir :

- contenu complet payé ;
- données clients ;
- accès réels ;
- liens sensibles ;
- secrets.

---

## KPI autorisés

KPI autorisés dans les JSON publics ou semi-internes :

- vues agrégées ;
- clics agrégés ;
- clics vers Stripe ;
- ventes attribuées agrégées ;
- taux de conversion agrégé ;
- formations demandées ;
- commentaires agrégés ;
- sauvegardes agrégées ;
- score santé produit ;
- score risque ;
- score priorité ;
- score prêt à vendre ;
- formations à améliorer ;
- formations à mettre à jour ;
- formations publiées ;
- formations à créer.

KPI interdits dans GitHub public :

- ventes par client ;
- données clients ;
- emails ;
- factures individuelles ;
- informations bancaires ;
- logs privés ;
- détails de support identifiables.

---

## Bundles

Les bundles doivent rester simples.

Règles :

- 2 à 5 formations complémentaires ;
- prix clair ;
- économie visible ;
- aucune complexité d’abonnement ;
- aucun contenu supplémentaire lourd si le bundle est seulement un regroupement ;
- KPI de panier moyen ;
- KPI de réachat ;
- KPI de conversion bundle.

Exemples :

```txt
Pack IA + Productivité
Pack Business express
Pack Finances simples
Pack Créateur digital débutant
```

---

## SEO

Chaque formation doit contenir :

- titre SEO unique ;
- méta-description unique ;
- slug propre ;
- mot-clé principal ;
- 3 à 7 mots-clés secondaires ;
- question cible ;
- image alt ;
- FAQ unique ;
- formations complémentaires ;
- statut `indexable`.

Règle : ne pas indexer une formation non publiée.

---

## Recommandations Craig

Les recommandations doivent respecter ces règles :

- recommander seulement les formations publiées ou clairement bientôt disponibles ;
- ne pas promettre un résultat garanti ;
- recommander selon le problème du visiteur ;
- proposer une prochaine étape logique ;
- éviter les formations non prêtes ;
- indiquer clairement si une formation n’est pas encore disponible.

---

## Ludite — données marketing autorisées

Pour chaque formation publiée, les données marketing peuvent contenir :

- 3 scripts YouTube Shorts ;
- 3 scripts Instagram Reels ;
- 3 publications X ;
- 2 accroches de vente ;
- 2 objections ;
- 2 réponses aux objections ;
- 1 email court ;
- 1 DM propre ;
- 1 angle éducatif ;
- CTA vers la formation.

Ne jamais inventer de témoignages.

---

## Hubert — support non sensible

Les données support autorisées :

- FAQ générale ;
- scripts génériques ;
- délais de réponse ;
- catégories de problèmes ;
- procédure de compensation ;
- procédure d’escalade.

Les données support interdites :

- nom du client ;
- email ;
- preuve de paiement ;
- conversation complète ;
- plainte identifiable ;
- détails privés.

---

## Adrien — pilotage

Adrien peut utiliser les données du dossier `data/` pour :

- prioriser les formations ;
- calculer les scores ;
- détecter les blocages ;
- suggérer la prochaine action ;
- suivre les KPI non sensibles ;
- afficher les feux rouge/jaune/vert ;
- produire des rapports agrégés ;
- identifier les formations à améliorer ;
- recommander des snapshots.

Adrien doit escalader à Olivier :

- sujet légal ;
- sujet financier sensible ;
- sujet santé ;
- plainte agressive ;
- double paiement ;
- remboursement complexe ;
- risque de réputation ;
- risque de sécurité ;
- contenu potentiellement trop prometteur.

---

## Routines de maintenance du dossier `data/`

### Routine quotidienne légère

- vérifier que le JSON principal n’est pas cassé ;
- vérifier la prochaine action prioritaire ;
- ne modifier qu’un point important à la fois ;
- sauvegarder avant grosse modification.

### Routine hebdomadaire

- vérifier les statuts ;
- vérifier les formations à améliorer ;
- vérifier les formations prêtes ;
- vérifier les champs vides critiques ;
- exporter un snapshot ;
- mettre à jour le dashboard non sensible.

### Routine mensuelle

- réviser les scores qualité ;
- réviser les scores rentabilité ;
- réviser les priorités ;
- vérifier les liens Stripe publics ;
- vérifier les pages après paiement ;
- vérifier les dates de mise à jour ;
- archiver les fichiers inutiles ;
- documenter les décisions.

---

## Ne pas modifier sans snapshot

Ces fichiers doivent toujours être sauvegardés avant une modification importante :

```txt
formations-index.json
dashboard-formations.json
bundles.json
seo.json
recommandations.json
actions-pivot-integrees.json
```

Avant modification :

1. exporter ou copier le fichier ;
2. vérifier que le JSON est valide ;
3. noter la raison du changement ;
4. faire la modification ;
5. tester le site ;
6. refaire un snapshot si tout fonctionne.

---

## Sauvegardes et snapshots

Avant chaque grosse modification :

1. copier le fichier JSON principal ;
2. exporter un snapshot ;
3. noter la date ;
4. noter ce qui change ;
5. conserver une version de secours ;
6. tester le site après modification.

Nom recommandé :

```txt
formations-index-snapshot-aaaa-mm-jj.json
```

---

## Validation JSON

Avant de publier une modification :

- vérifier que le JSON est valide ;
- vérifier les virgules ;
- vérifier les guillemets ;
- vérifier les crochets ;
- vérifier les accolades ;
- vérifier les champs critiques ;
- vérifier les catégories ;
- vérifier les statuts ;
- vérifier les liens publics ;
- vérifier l’absence de données sensibles.

---

## Règle anti-chaos

Ne pas ajouter un fichier si :

- son rôle n’est pas clair ;
- il duplique un fichier existant ;
- il contient des données sensibles ;
- il n’est utilisé par aucune page ;
- il crée une nouvelle version concurrente ;
- il n’a pas de propriétaire clair ;
- il n’aide pas à vendre, livrer, mesurer ou améliorer.

---

## Première priorité réelle

Ne pas créer 400 fiches tout de suite.

La priorité est :

```txt
1 formation complète
+ 1 fiche publique
+ 1 checklist
+ 1 lien Stripe
+ 1 page après paiement
+ 1 accès testé
+ 1 support prêt
+ 1 vente test
```

Formation pilote recommandée :

```txt
Utilise l’IA pour sauver 3 heures par semaine
```

---

## Checklist avant commit

Avant de cliquer sur `Commit changes`, vérifier :

- [ ] Le fichier est dans le bon dossier.
- [ ] Le nom est en minuscules.
- [ ] Le nom ne contient pas d’accent.
- [ ] Le JSON est valide.
- [ ] Aucun secret n’est présent.
- [ ] Aucun email client n’est présent.
- [ ] Aucun contenu payant complet n’est exposé.
- [ ] Les catégories sont officielles.
- [ ] Les statuts sont officiels.
- [ ] Les liens publics fonctionnent.
- [ ] Les champs critiques sont remplis.
- [ ] Le dashboard reste non sensible.
- [ ] Le site fonctionne après commit.

---

## Note de sécurité finale

Ce dossier est une base de données publique ou semi-publique de pilotage. Il est utile pour organiser, afficher, recommander et mesurer, mais il ne remplace pas :

- une vraie base de données ;
- une authentification ;
- un espace membre sécurisé ;
- un CRM privé ;
- un dashboard serveur ;
- une validation légale ou comptable.

Le dossier `data/` doit rester clair, propre, prudent et utile.
