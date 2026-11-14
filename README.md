# Formulaire interne, variante ALIAS

Copie du widget « Formulaire interne » (`https://github.com/gristgouv/grist-cw-intra-form`, commit `65c4f6a` du 10 novembre 2026,
auteur maluhialoha), avec un seul changement, dans `app.js` (chercher « ALIAS »).

Le widget d'origine lit le type des colonnes dans `_grist_Tables_column`. Grist refuse cette lecture à qui ne lit pas tout
le document : sous des règles d'accès à périmètre, le formulaire n'a plus ni listes déroulantes ni sélecteurs de date.
Cette variante lit alors le type des colonnes dans le réglage du widget, sous la clé `columnsMeta`, que `scripts/alias.py`
écrit à partir du schéma. Quand la lecture des métadonnées est permise, rien ne change.

Les polices du dossier `fonts/` d'origine ne sont pas reprises : sans elles le widget utilise la police par défaut.
À proposer à l'auteur ; d'ici là, la variante doit être servie à une adresse à nous et ajoutée comme widget personnalisé.
