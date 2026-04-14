# 🎾 TennisFlash

> Service de cordage de raquettes à la demande avec pickup et livraison.

---

## Le problème

Quand un joueur de tennis casse son cordage, il doit :

- Trouver un cordeur disponible
- Se déplacer en magasin ou en atelier
- Laisser sa raquette et revenir la chercher 24 à 72h plus tard
- Parfois annuler sa session de jeu faute de raquette prête à temps

En Île-de-France, il n'existe aucun service 100% digital permettant de commander un recordage en quelques clics avec pickup et livraison à domicile.

## La solution

**TennisFlash** est un micro-SaaS qui permet aux joueurs de tennis de commander un recordage de raquette en ligne. Un cordeur se déplace en scooter pour récupérer la raquette, la corder et la livrer — le tout en 24h (standard) ou 4h (express).

## Public cible

- Joueurs de tennis réguliers (compétiteurs, loisirs avancés) en Île-de-France
- Clubs de tennis et coachs indépendants
- Joueurs qui n'ont pas le temps de se déplacer en atelier

## Fonctionnalité principale

**Commande de cordage en ligne avec pickup & livraison à domicile.**

Le joueur choisit son cordage, sa tension, son créneau de pickup — et c'est tout. Il suit sa commande en temps réel via notifications SMS.

## Fonctionnalités secondaires

- **Suivi de commande en temps réel** — statuts : récupérée → en cours de cordage → en livraison → livrée
- **Paiement en ligne sécurisé** — Stripe
- **Historique des raquettes** — le joueur enregistre ses raquettes (modèle, cordage préféré, tension) pour recommander en 1 clic
- **Dashboard admin** — gestion des commandes, planning des tournées, suivi du CA

## Analyse concurrentielle

| Concurrent | Modèle | Point faible |
|---|---|---|
| Éclair Cordage | Réseau de cordeurs à domicile | UX datée, pas de paiement en ligne |
| Multioumono | Boutique + livraison vélo Paris 14e | Limité à Paris, pas de webapp |
| SportSystem | Magasin + coursier Paris intra-muros | Service secondaire, formulaire basique |
| Tennis Cordage Express | Cordeur indépendant | Site vitrine, pas de suivi en ligne |

**Avantage TennisFlash** : 100% digital, mobile-first, paiement intégré, suivi temps réel, couverture IDF (scooter > vélo).

## Tarifs

| Formule | Délai | Prix |
|---|---|---|
| Standard | 24h | 35€ (cordage + pose + livraison) |
| Express | 4h | 50€ (cordage + pose + livraison) |

## Stack technique

| Couche | Technologie | Justification |
|---|---|---|
| Frontend | **Next.js** + **Tailwind CSS** + **shadcn/ui** | SSR, performance, UI moderne et rapide à développer |
| Backend | **NestJS** + **TypeScript** | Architecture modulaire, typage fort, écosystème Node.js |
| ORM | **Prisma** | Migrations, typage auto, requêtes SQL lisibles |
| Base de données | **PostgreSQL** | Relationnelle, robuste, gratuite — adapté au SQL exigé pour le CDA |
| Paiement | **Stripe** | Standard du marché, SDK bien documenté |
| Notifications | **Twilio** | SMS fiables, API simple |


## Charte graphique

### Palette de couleurs

| Couleur | Hex | Rôle |
|---|---|---|
| Blanc | `#FFFFFF` | Fond principal |
| Bleu nuit | `#0F172A` | Headers, hero, textes forts |
| Noir | `#1A1A1A` | Textes courants |
| Vert flash | `#AAFF00` | Boutons CTA, accents, éléments interactifs |
| Gris clair | `#F5F5F5` | Fonds secondaires, cartes |
| Gris moyen | `#6B7280` | Textes secondaires |

### Typographies

| Élément | Font | Taille | Poids |
|---|---|---|---|
| H1 | Poppins | 32px | Bold (700) |
| H2 | Poppins | 24px | Bold (700) |
| H3 | Poppins | 18px | Semi-bold (600) |
| Corps | DM Sans | 16px | Regular (400) |
| Petit texte | DM Sans | 14px | Regular (400) |
| Boutons | DM Sans | 16px | Semi-bold (600) |

### Ambiance visuelle

Clean, aéré, mobile-first. Fond blanc dominant avec touches de vert flash sur les éléments d'action. Headers en bleu nuit pour le contraste. Style sport/tech moderne, inspiré des apps de service à la demande (Uber, Deliveroo).

## Wireframes

Voir le dossier [`/wireframes`](./wireframes/)

## Diagramme de cas d'utilisation

Voir le dossier [`/use-case-diagram`](./use-case-diagram/)

## Structure du repo

```
/
├── README.md
├── slides/
├── wireframes/
└── use-case-diagram/
```

---

