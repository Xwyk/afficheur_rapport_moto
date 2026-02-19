# Afficheur Rapport Moto - TDM850

Projet de circuit imprimé pour afficheur 7 segments indiquant le rapport de boîte engagé sur une moto Yamaha TDM850.

## Caractéristiques

- **Moto cible** : Yamaha TDM850
- **Rapports affichés** : N, 1, 2, 3, 4, 5 (5 vitesses + neutre)
- **Type d'afficheur** : 7 segments à anode commune
- **Commande** : Masse commutée par le sélecteur de vitesse

## Principe de fonctionnement

Le sélecteur de vitesse de la TDM850 commute la masse vers le contact correspondant au rapport engagé. Le circuit utilise cette information pour allumer les segments appropriés de l'afficheur.

### Logique d'affichage

| Rapport | Segments allumés |
|---------|------------------|
| N (Neutre) | a, b, c, d, e, f |
| 1 | b, c |
| 2 | a, b, g, e, d |
| 3 | a, b, g, c, d |
| 4 | f, g, b, c |
| 5 | a, f, g, c, d |

## Fichiers du projet

| Fichier | Description |
|---------|-------------|
| `afficheur_moto_smd.fzz` | Projet Fritzing (source) |
| `afficheur_moto_smd_schéma.png` | Schéma électronique |
| `afficheur_moto_smd_bb.png` | Vue breadboard |
| `afficheur_moto_smd_circuit imprimé.png` | Tracé du PCB |
| `afficheur_moto_smd_bom.html` | Liste des composants (BOM) |
| `afficheur_moto_smd_d356a.ipc` | Fichier IPC pour fabrication |

## Composants principaux

- Afficheur 7 segments à anode commune
- Diodes de signal (pour la matrice de décodage)
- Résistances de limitation de courant
- Connecteur pour raccordement au sélecteur

## Alimentation

- Tension : 12V (batterie moto)
- Protection : Prévoir un fusible et protection contre les pics de tension

## Notes d'installation

1. Identifier les fils du sélecteur de vitesse sur la moto
2. Connecter chaque entrée du circuit au fil correspondant du sélecteur
3. Assurer une bonne masse commune
4. Protéger le circuit de l'humidité et des vibrations

## Licence

Projet personnel - Usage libre
