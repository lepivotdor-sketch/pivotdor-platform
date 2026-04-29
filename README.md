# Le Pivot d’Or — Mini Mini Formation

**Site GitHub Pages officiel du projet Mini Mini Formation / Le Pivot d’Or.**

Ce dépôt contient la base publique du site web : pages HTML, styles, scripts, structure SEO, pages légales, accès client de démonstration, espace client, formation privée de démonstration et fichiers techniques comme `robots.txt`, `sitemap.xml` et `404.html`.

> **Mission du projet :** bâtir un système clair, accessible et rentable pour vendre des mini-formations et produits digitaux à achat unique, autour de l’IA, la productivité, l’apprentissage, le business, les finances, les relations, le bonheur et la santé.

---

## 1. Vision du projet

Le projet vise à créer un catalogue public de mini-formations numériques vendues entre **5 $ et 50 $**, sans coaching obligatoire, avec une expérience simple :

1. Le visiteur découvre une formation.
2. Il consulte une page claire.
3. Il achète avec Stripe.
4. Il reçoit un accès client.
5. Il consulte la formation dans un espace privé.
6. Il suit sa progression.
7. Il peut demander du support si nécessaire.

Le site doit rester **simple, rapide, premium, noir et or, accessible et facile à maintenir**.

---

## 2. Positionnement officiel

**Nom public :** Le Pivot d’Or  
**Projet interne :** Mini Mini Formation  
**Style :** futuriste accessible, premium, clair, structuré  
**Slogan officiel :** Bâtir une vie solide : Vision. Clarté. Discipline. Structure. Constance.

---

## 3. Catégories officielles

Les 8 catégories principales du catalogue sont :

1. IA
2. Productivité
3. Apprentissage
4. Business
5. Finances
6. Relations
7. Bonheur
8. Santé

Priorité de lancement :

1. IA
2. Productivité
3. Business
4. Finances

---

## 4. Modèle économique

Le site repose sur des achats uniques, sans abonnement et sans coaching obligatoire.

| Prix | Type de produit | Contenu attendu |
|---:|---|---|
| 5 $ | Micro-guide / checklist | PDF court ou checklist très simple |
| 15 $ | Mini-formation courte | Contenu court + checklist |
| 25 $ | Mini-formation + outils | Formation + modèles + checklist |
| 50 $ | Mini-système complet | Formation + modèles + plan d’action + outils |

**Règle commerciale :** vente finale après activation de l’accès. Une compensation raisonnable peut être offerte sous forme de formations gratuites, sans exposer le contenu complet publiquement.

---

## 5. Pages principales du dépôt

### Pages publiques indexables

Ces pages peuvent être visibles par les moteurs de recherche :

- `index.html` — accueil
- `formations.html` — catalogue public
- `contact.html` — contact
- `support.html` — support
- `conditions.html` — conditions de vente et d’utilisation
- `confidentialite.html` — politique de confidentialité
- `vente-finale.html` — explication de la vente finale

### Pages à ne pas indexer

Ces pages doivent rester hors SEO :

- `acces.html` — accès client local de démonstration
- `espace-client.html` — espace client local de démonstration
- `formation-privee.html` — formation privée de démonstration
- `merci.html` — page après paiement
- `404.html` — page d’erreur

Ces pages doivent utiliser une balise du type :

```html
<meta name="robots" content="noindex, nofollow" />
```

---

## 6. Structure recommandée du dépôt

```text
pivotdor-platform/
│
├── index.html
├── formations.html
├── contact.html
├── support.html
├── conditions.html
├── confidentialite.html
├── vente-finale.html
├── acces.html
├── espace-client.html
├── formation-privee.html
├── merci.html
├── 404.html
├── robots.txt
├── sitemap.xml
├── README.md
├── .nojekyll
├── logo.png
│
├── css/
│   ├── style.css
│   ├── responsive.css
│   ├── catalogue.css
│   ├── pages.css
│   └── print.css
│
├── js/
│   ├── main.js
│   ├── navigation.js
│   ├── catalogue.js
│   ├── logo-fallback.js
│   ├── acces.js
│   └── dashboard.js
│
├── data/
│   ├── formations.json
│   ├── categories.json
│   └── produits.json
│
├── formations/
│   └── pages-publiques-ou-apercus/
│
├── produits/
│   └── fichiers-non-sensibles-ou-apercus/
│
├── templates/
│   └── modeles-publics-ou-exemples/
│
├── assets/
│   ├── images/
│   ├── icones/
│   └── internes/
│
├── agents/
│   ├── craig/
│   ├── hubert/
│   ├── ludite/
│   └── manus/
│
├── marketing/
│   ├── contenus/
│   ├── emails/
│   └── scripts/
│
├── stripe/
│   └── notes-integration.md
│
├── legal/
│   └── brouillons/
│
├── dashboard/
│   └── interface-interne-demo/
│
├── sauvegardes/
│   └── snapshots-locaux/
│
└── docs/
    └── documentation-interne/
```

---

## 7. Règles de sécurité importantes

GitHub Pages est excellent pour publier un site statique, mais ce n’est pas un coffre-fort.

Ne jamais placer dans ce dépôt public :

- de vrais mots de passe ;
- des clés API ;
- des clés Stripe secrètes ;
- des données clients ;
- des courriels clients ;
- des fichiers payants complets ;
- des exports de ventes ;
- des fichiers comptables ;
- des liens privés permanents ;
- des données sensibles dans des fichiers JSON publics.

Les pages `acces.html`, `espace-client.html` et `formation-privee.html` sont des **interfaces de démonstration**. Pour une vraie version commerciale, elles devront être connectées à :

- une authentification réelle ;
- une validation Stripe côté serveur ;
- une base de données ;
- des liens temporaires sécurisés ;
- un stockage privé pour les fichiers payants.

---

## 8. Règles SEO

Le SEO doit pousser les pages publiques, pas les zones privées.

### À indexer

- Accueil
- Catalogue
- Pages de vente publiques
- Contact
- Support
- Conditions
- Confidentialité
- Vente finale

### À ne pas indexer

- Accès client
- Espace client
- Formation privée
- Page merci
- Dashboard
- Agents
- Data
- Stripe
- Sauvegardes
- Fichiers internes

Le fichier `robots.txt` doit pointer vers :

```text
Sitemap: https://lepivotdor-sketch.github.io/pivotdor-platform/sitemap.xml
```

---

## 9. Règles de nommage des fichiers

Pour éviter les erreurs 404 :

- utiliser des noms courts ;
- éviter les accents dans les noms de fichiers ;
- utiliser des minuscules ;
- utiliser des tirets au lieu des espaces ;
- toujours finir les pages par `.html` ;
- garder les liens internes identiques au nom réel du fichier.

Exemples corrects :

```text
conditions.html
confidentialite.html
vente-finale.html
espace-client.html
formation-privee.html
```

Exemples à éviter :

```text
conditionalite.html
Confidentialité.html
vente finale.html
formation privée.html
page2.html
```

---

## 10. Déploiement GitHub Pages

Étapes recommandées :

1. Ouvrir le dépôt GitHub.
2. Vérifier que les fichiers sont à la racine du dépôt.
3. Commiter les changements.
4. Aller dans **Settings**.
5. Aller dans **Pages**.
6. Choisir la branche publiée.
7. Vérifier que le site est accessible à :

```text
https://lepivotdor-sketch.github.io/pivotdor-platform/
```

8. Tester les pages principales une par une.
9. Tester les liens internes.
10. Corriger toute erreur 404.

---

## 11. Checklist avant chaque commit

Avant de cliquer sur **Commit changes**, vérifier :

- [ ] Le fichier porte le bon nom.
- [ ] Le fichier est au bon endroit.
- [ ] Le fichier contient bien `<!DOCTYPE html>` si c’est une page HTML.
- [ ] Les liens internes pointent vers les bons fichiers.
- [ ] Les pages privées ont `noindex, nofollow`.
- [ ] Aucun secret n’est dans le code.
- [ ] Aucune donnée client n’est dans le dépôt.
- [ ] Les boutons importants fonctionnent.
- [ ] Le site fonctionne sur mobile.
- [ ] La page 404 est présente.
- [ ] `robots.txt` est à jour.
- [ ] `sitemap.xml` est à jour.

---

## 12. Checklist de test après publication

Après un commit, tester :

- [ ] Accueil : `/`
- [ ] Catalogue : `/formations.html`
- [ ] Contact : `/contact.html`
- [ ] Support : `/support.html`
- [ ] Conditions : `/conditions.html`
- [ ] Confidentialité : `/confidentialite.html`
- [ ] Vente finale : `/vente-finale.html`
- [ ] Accès client : `/acces.html`
- [ ] Espace client : `/espace-client.html`
- [ ] Formation privée : `/formation-privee.html`
- [ ] Merci : `/merci.html`
- [ ] Page 404 avec une fausse URL
- [ ] Logo
- [ ] Navigation mobile
- [ ] Boutons Stripe, s’ils sont ajoutés

---

## 13. Agents IA prévus

Le projet prévoit plusieurs agents ou rôles IA :

### Craig

Recommande les formations selon le problème du visiteur.

### Hubert

Gère le support client, les paiements, les accès, les demandes raisonnables et les compensations.

### Ludite

Crée les contenus marketing : scripts courts, publications, DM, idées de vidéos, angles de vente, objections et calendriers.

### Manus

Aide à concevoir, structurer et améliorer les pages, systèmes et automatisations.

---

## 14. Stripe

Stripe doit être utilisé pour les paiements.

Important :

- les liens publics Stripe peuvent être dans les boutons ;
- les clés secrètes Stripe ne doivent jamais être dans GitHub ;
- la validation d’achat réelle doit se faire côté serveur ;
- la page `merci.html` ne doit pas donner accès à du contenu payant complet sans vérification.

---

## 15. Progression client

La progression locale peut être simulée dans le navigateur avec `localStorage`, mais ce n’est pas une vraie base de données.

Pour une vraie plateforme :

- chaque client doit avoir un compte ;
- chaque achat doit être lié à Stripe ;
- la progression doit être enregistrée côté serveur ;
- les accès doivent pouvoir être révoqués ;
- les formations doivent être associées au bon client.

---

## 16. Mises à jour des formations

Chaque formation doit avoir :

- date de création ;
- dernière mise à jour ;
- prochaine mise à jour ;
- version ;
- statut ;
- note qualité ;
- note rentabilité.

Règle : **une mise à jour annuelle obligatoire par formation.**

---

## 17. Dashboard caché

Le dashboard caché doit afficher les indicateurs essentiels :

- formations en ligne ;
- ventes ;
- visites ;
- clics ;
- taux de conversion ;
- accès activés ;
- problèmes d’accès ;
- contenus performants ;
- notes qualité ;
- notes rentabilité ;
- mises à jour à faire ;
- prochaines actions.

Attention : tant qu’il n’y a pas de vraie authentification serveur, le dashboard ne doit contenir aucune donnée sensible.

---

## 18. Jumeau numérique interne des formations

Le projet prévoit un jumeau numérique interne des formations : une représentation de gestion des 400 formations prévues.

Chaque formation peut avoir :

- ID ;
- titre ;
- catégorie ;
- prix ;
- statut ;
- version ;
- score qualité ;
- score rentabilité ;
- nombre de vues ;
- nombre de ventes ;
- taux de conversion ;
- lien Stripe ;
- prochaine mise à jour ;
- kit marketing ;
- prochaine action.

Ce jumeau numérique ne doit pas exposer le contenu payant complet dans GitHub public.

---

## 19. Standards visuels

Le style du site doit respecter :

- noir et or ;
- design premium ;
- boutons visibles ;
- textes clairs ;
- sections aérées ;
- mobile-first ;
- lisibilité forte ;
- aucune surcharge inutile ;
- ton direct au **tu** ;
- logique de clarté, discipline, structure et constance.

---

## 20. Priorités actuelles

Priorités recommandées pour continuer :

1. Stabiliser les pages publiques.
2. Vérifier tous les liens internes.
3. Ajouter ou corriger `contact.html` si nécessaire.
4. Créer les premières pages publiques de formations.
5. Préparer les liens Stripe.
6. Garder les pages privées en mode démonstration.
7. Créer un vrai système sécurisé plus tard.
8. Mettre à jour `sitemap.xml` quand une page publique est ajoutée.
9. Mettre à jour `robots.txt` quand une zone privée est ajoutée.
10. Tester le site après chaque commit.

---

## 21. Limites actuelles

Ce site est une base statique GitHub Pages.

Il ne fait pas encore :

- authentification réelle ;
- validation Stripe réelle côté serveur ;
- gestion de compte client réelle ;
- progression multi-appareils ;
- base de données ;
- protection complète du contenu payant ;
- analytics serveur ;
- automatisation complète du support.

Ces éléments devront être ajoutés progressivement avec une architecture plus avancée.

---

## 22. Règle d’or du projet

> Le site public doit vendre, rassurer et orienter.  
> Le contenu payé complet doit être protégé.  
> Les fichiers internes ne doivent jamais être exposés par erreur.  
> Chaque page doit aider le visiteur à faire une action claire.

---

## 23. Version

```text
Projet : Le Pivot d’Or — Mini Mini Formation
Dépôt : pivotdor-platform
Version README : 1.0
Dernière mise à jour : 2026-04-28
Statut : Base GitHub Pages publique en construction
```

---

## 24. Note interne

Ce README doit être mis à jour chaque fois que :

- une nouvelle page publique est ajoutée ;
- une nouvelle zone privée est créée ;
- un lien Stripe est ajouté ;
- une formation publique est publiée ;
- le sitemap change ;
- le robots.txt change ;
- la structure du dépôt change ;
- le site passe d’une version statique à une version sécurisée avec serveur.
mise a jours teste
