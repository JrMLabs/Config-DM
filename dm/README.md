# Paquet LeDM

Ce dossier reçoit automatiquement le DM chiffré publié par le gestionnaire PC du dépôt privé `LeDM`.

Fichiers utilisés :

- `documentation.enc` : unique fichier DM chiffré en AES-256-GCM ; il est remplacé à chaque nouvelle publication.
- `version.json` : indique si un fichier est disponible, son numéro de version et son SHA-256.

Quand le DM publié est supprimé, `documentation.enc` est retiré et `version.json` passe à `status: "fichier absent"`.

La clé AES de déchiffrement n'est jamais stockée dans ce dépôt public.
