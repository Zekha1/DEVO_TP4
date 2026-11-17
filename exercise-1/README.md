# Apprentissages

## 1. Répartir les pods (Topology Spread Constraints)

Répartir les pods du guestbook entre les nœuds.

### Problème rencontré et pourquoi il est survenu

Aucun problème.

### Solution appliquée et pourquoi cette solution fonctionne

Ajout d'une `TopologySpreadConstraint` dans le Deployment.

La commande `helm upgrade` applique la modification.
Les trois pods sont répartis avec deux pods sur un nœud et un pod sur l'autre.

### Ce que j'ai appris

Les pods ne sont pas forcément répartis automatiquement.
Les `TopologySpreadConstraints` permettent de mieux répartir les pods.

La commande `kubectl drain` évacue les pods d'un nœud.
La commande `kubectl uncordon` remet le nœud en service.
