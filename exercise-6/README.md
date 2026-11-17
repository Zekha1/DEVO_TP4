# Apprentissages

## 6. Provoquer des pannes avec Chaos Mesh

Tester la résistance du guestbook à différentes pannes.

### Problème rencontré et pourquoi il est survenu

Aucun problème particulier.

### Solution appliquée et pourquoi cette solution fonctionne

Chaos Mesh a été installé avec Helm.
Une expérience `PodChaos` a supprimé un pod du guestbook.
Le Deployment l'a recréé automatiquement.
Une expérience `NetworkChaos` a ajouté 500 ms de latence à Redis.
La latence des requêtes a augmenté dans Grafana.

### Ce que j'ai appris

J'ai appris à simuler une panne avec Chaos Mesh.
Un Deployment recrée un pod supprimé.
La latence réseau dégrade directement les performances de l'application.
