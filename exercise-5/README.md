# Apprentissages

## 5. Définir un SLO et alerter dessus

Définir des objectifs de disponibilité et créer des alertes.

### Problème rencontré et pourquoi il est survenu

Aucun problème particulier.

### Solution appliquée et pourquoi cette solution fonctionne

Un SLO de 99 % de disponibilité a été défini.
Des alertes ont été créées pour les erreurs HTTP, l’arrêt du Guestbook et
l’indisponibilité de Redis.
Alertmanager a été configuré pour recevoir les alertes.

### Ce que j'ai appris

J’ai appris à utiliser un budget d’erreur et le burn rate.
J’ai aussi appris à créer des alertes Prometheus et à tester une panne de
Redis.
