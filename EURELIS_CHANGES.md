# EURELIS_CHANGES

Registre des écarts de la branche `eurelis/main` par rapport à la version
d'Open WebUI sur laquelle elle est posée. Une ligne par modification, avec sa
raison et son sort en amont. Chaque écart est marqué `# EURELIS:` dans le code.

Base actuelle : **v0.12.0** (`15818d88f`).

| Fichier | Modification | Raison | Branche amont | Statut amont |
|---|---|---|---|---|
| `backend/open_webui/utils/oauth.py` (`_preflight_authorization_url`) | Une réponse portant `cf-mitigated` n'invalide plus le client OAuth | Le défi anti-robot de Cloudflare devant `www.canva.com` recopie l'URL (donc `redirect_uri`) : faux positif, « OAuth client registration is still invalid after re-registration », connecteur Canva MCP inutilisable | `fix/oauth-preflight-bot-challenge` (sur `dev`) | Corrigé sur `dev` le 2026-10-13 (commit `4f9f04ce`), non publié : retirer cet écart au rebase sur la release qui le contient |
