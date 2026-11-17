# Apprentissages

## 2. Déployer la stack Prometheus

Installer Prometheus, Grafana et Alertmanager avec Helm.

### Problème rencontré et pourquoi il est survenu

Aucun problème.

### Solution appliquée et pourquoi cette solution fonctionne

Ajout du dépôt Helm `prometheus-community`.
Installation de `kube-prometheus-stack` dans le namespace `monitoring`.

### Ce que j'ai appris

J’ai appris à installer une stack de supervision avec Helm et découvert les dashboards Grafana et les requêtes PromQL.