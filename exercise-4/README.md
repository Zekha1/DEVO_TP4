# Apprentissages

## 4. Construire un dashboard RED

Créer un dashboard Grafana pour suivre le débit, les erreurs et la latence du
guestbook.

### Problème rencontré et pourquoi il est survenu

Aucun problème particulier.

### Solution appliquée et pourquoi cette solution fonctionne

Un dashboard `Guestbook RED` a été créé avec trois panels :

- **Rate** : `sum by (handler) (rate(http_requests_total{handler!~"/healthz|/metrics|static"}[5m]))`
- **Errors** : pourcentage des réponses `5xx` avec `or vector(0)`.
- **Duration** : p50, p95 et p99 avec `histogram_quantile`.

Le test k6 a généré environ 200 requêtes par seconde pendant la charge.
Le nombre d'erreurs est resté à 0.
La latence est restée faible et stable.

### Ce que j'ai appris

J'ai appris à créer un dashboard RED avec Grafana.
Le p99 permet de voir les requêtes les plus lentes.
Les métriques Prometheus permettent de suivre l'effet de la charge.

![Dashboard Grafana](<dashboard.png>)