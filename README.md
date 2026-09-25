# MA3 Mods

Mods de l'interface native grandMA3, installables et désinstallables depuis la console avec le plugin **MA3 Mods**
(Tensegrity Lighting Service — Florian Declercq).

Ce dépôt sert de source de mises à jour au plugin :

| Fichier | Rôle |
|---|---|
| `catalog.lua` | liste des mods publiés (version, taille, empreinte) et version du plugin |
| `packages/*.ma3mod` | paquets de mods, **chiffrés** : lisibles uniquement avec le mot de passe MA3 Mods |
| `plugin/MA3Mods.xml` | plugin MA3 Mods (moteur, sans mods) à importer dans le show |

## Fonctionnement
- Le plugin ne contient aucun mod ; les mods sont copiés sur une clé USB (`FDPlugins/MA3Mods/`).
- Les mods sont posés par petits blocs dans les fichiers de l'interface MA, chacun précédé d'un marqueur qui contient
  les lignes d'origine : désinstallation et « Restaurer la console » fonctionnent toujours, même sans la clé, et les
  modifications d'autres plugins sont préservées.
- La mise à jour est manuelle (bouton), protégée par mot de passe, et ne contacte GitHub que si la station a accès à
  Internet.
- Un redémarrage de MA est nécessaire après chaque changement.

Versions de MA validées : 2.5.0.3, 2.5.1.0.
