1) README.md (modèle complet — Français)
Aerodrome — Protocole de lending sur Basechain
Résumé

Aerodrome est un protocole de lending/borrowing construit sur Basechain.
Ce dépôt contient le code, la documentation et les scripts nécessaires pour déployer et tester le protocole.

Table des matières

Installation
Architecture
Usage
Tests
Contribuer
Licence

Installation

Cloner le repo :
git clone https://github.com/TON_COMPTE/aerodrome.git
Se placer dans le dossier :
cd aerodrome
Installer les dépendances :
npm installou
yarn install

Configuration

Copier l’exemple d’environnement et compléter :
cp .env.example .env
Variables importantes :
RPC_URL: RPC Basechain
PRIVATE_KEY: clé privée pour le deploy (ne pas committer)
ETHERSCAN_API_KEY / BASESCAN_API_KEY (si nécessaire)



Architecture

contracts/: smart contracts Solidity
scripts/: scripts de déploiement et utilitaires
tests/: tests unitaires / intégration
docs/: documentation utilisateur et design

Usage (local)

Démarrer un network local (ex: Anvil, Hardhat):
npx hardhat node
Déployer en local :
npx hardhat run --network localhost scripts/deploy.js
Lancer les tests :
npx hardhat test

Bonnes pratiques sécurité

Ne jamais pousser les clés privées ni secrets.
Faire des audits externes avant mainnet.
Utiliser des multisigs pour l’administration en production.

Contribuer

Voir CONTRIBUTING.md pour le guide de contribution.
Ouvrir une issue pour discuter des changements majeurs.

Licence

Spécifier la licence (ex : MIT). Voir LICENSE.


2) CONTRIBUTING.md (modèle — Français)
Contribuer au projet Aerodrome
Merci de l’intérêt ! Avant de proposer des changements, merci de suivre ces étapes :

Forker le dépôt et créer une branche à partir de main :
git checkout -b feat/ma-fonctionnalite
Faire des commits clairs et atomiques :
Format suggéré : type(scope): courte description
Exemple : feat(core): ajout du calcul d’intérêt variable


Tests
Ajouter/mettre à jour les tests correspondants dans tests/
S’assurer que tous les tests passent localement : npx hardhat test


Linter / Format
Respecter le style du projet : npx eslint . && npx prettier --check .


Ouvrir une Pull Request
Remplir le template de PR (fournir but, approches alternatives, sécurité, tests).
Répondre aux revues et demandes de modifications.