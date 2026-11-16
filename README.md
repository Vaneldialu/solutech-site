# SoluTech – Site vitrine

Site web de **SoluTech**, agence digitale spécialisée dans les solutions digitales : automatisation des tâches, création de sites web, applications web et mobiles.

Le site met en avant l'**audit gratuit** et permet aux visiteurs de contacter l'agence par **WhatsApp** ou par **e-mail**.

## Contenu de la page

| Section | Rôle |
|---|---|
| En-tête | Logo, menu (menu « burger » sur téléphone) |
| Accueil | Accroche, bouton « Demander mon audit gratuit », exemple d'automatisation |
| Services | Automatisation, sites web, applications web et mobiles, design, chatbots/IA, maintenance |
| Audit gratuit | Présentation de l'audit en 3 étapes |
| Pourquoi SoluTech | 4 arguments de confiance |
| Questions fréquentes | 4 questions/réponses |
| Contact | Formulaire, e-mail, numéro WhatsApp |
| Bouton flottant | Accès direct à WhatsApp |

## Structure du dossier

```
solutech-site/
├── index.html            # Le site complet (HTML, CSS et JavaScript dans un seul fichier)
├── assets/
│   └── solutech-logo.png # Logo SoluTech, fond transparent
├── README.md             # Cette documentation
├── CHANGELOG.md          # Journal des modifications
└── .gitignore
```

Le site n'a aucune dépendance à installer : il suffit d'ouvrir `index.html` dans un navigateur.

## Paramètres à connaître

| Information | Valeur actuelle | À modifier dans `index.html` |
|---|---|---|
| Numéro WhatsApp | +243 89 161 35 34 (`243891613534`) | Chercher `243891613534` (3 endroits : bouton flottant, lien du contact, formulaire) |
| E-mail de réception | `vanel.dialundama@krispen.tech` | Chercher `krispen.tech` (lien du contact et formulaire) |
| E-mail affiché | `contact@solutech.com` | Chercher `contact@solutech.com` (texte du lien) |

## Fonctionnement du formulaire

Le site n'a pas de serveur : le formulaire ne stocke rien.

- **Envoyer sur WhatsApp** : ouvre `wa.me` avec un message prérempli (nom, e-mail, téléphone, besoin, audit gratuit, message). Le visiteur doit appuyer sur « Envoyer » dans WhatsApp.
- **Envoyer par e-mail** : ouvre la messagerie du visiteur avec un message prérempli adressé à l'e-mail de réception. Le visiteur doit appuyer sur « Envoyer ».
- Le nom, l'e-mail et le message sont obligatoires. Le téléphone est facultatif.

Pour recevoir les demandes automatiquement, il faudrait relier le formulaire à un service externe (par exemple Formspree) ou à un back-end.

## Publier avec GitHub Pages

1. Créer un dépôt vide sur GitHub (par exemple `solutech-site`), sans README.
2. Dans le dossier du projet :
   ```bash
   git remote add origin https://github.com/<votre-utilisateur>/solutech-site.git
   git branch -M main
   git push -u origin main
   ```
3. Sur GitHub : **Settings → Pages → Build and deployment → Deploy from a branch**, choisir `main` et `/ (root)`.
4. Le site sera disponible à l'adresse `https://<votre-utilisateur>.github.io/solutech-site/`.

## Règles pour les commits

Chaque modification fait l'objet d'un commit **en français** qui explique ce qui change et pourquoi.

- Titre court (moins de 70 caractères) commençant par un verbe : `Ajout`, `Modification`, `Correction`, `Suppression`.
- Une ligne vide, puis une liste qui détaille les changements.
- Chaque modification est aussi notée dans `CHANGELOG.md`.

Exemple :

```
Correction de l'envoi du formulaire par WhatsApp

- Utilisation de wa.me à la place de api.whatsapp.com
- Ajout d'un lien de secours si WhatsApp ne s'ouvre pas
```
