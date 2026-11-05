# MandamPro — template visuel

Template **UI-only** pour le client MandamPro, conforme au contrat
`onirtech.template-host.v1`.

- design inspiré de ChatGPT ;
- rendu des messages, médias et blocs `tool_search_result` ;
- aucune requête réseau, aucun accès à la base ou à l'API ;
- OTP email hors périmètre de ce premier lot.

## Développement

```bash
npm install
npm run dev       # harness MOCK, sans connexion réelle
npm test
npm run validate
npm run pack
```

## Intégration

Le template lit `ctx` et appelle uniquement `ctx.actions.*`. La recherche de
fiches et les médias sont fournis par l'hôte via les blocs du contrat.

Le package produit par `npm run pack` est une archive `.onirtech-template`
importable dans ONIR-CMS, puis rattachable à un lien chatbot.
