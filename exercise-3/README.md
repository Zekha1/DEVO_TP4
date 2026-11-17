# Apprentissages

## 3. Instrumenter le guestbook

Ajouter une métrique pour mesurer la durée des requêtes HTTP.

### Problème rencontré et pourquoi il est survenu

Prometheus n’affichait pas les métriques du Guestbook, le `ServiceMonitor` n’était pas correctement sélectionné.

### Solution appliquée et pourquoi cette solution fonctionne

Ajout de l’histogramme `http_request_duration_seconds`.
Création d’un `ServiceMonitor` pour exposer les métriques à Prometheus.

### Ce que j'ai appris

J’ai appris à créer un histogramme Prometheus et à utiliser un `ServiceMonitor` pour connecter une application à Prometheus.