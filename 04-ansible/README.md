
# Ansible - Automatisation Linux

## Objectif
Automatiser l'installation et la configuration du serveur web Nginx sur Ubuntu 22.04 avec Ansible.

## Environnement
- Ubuntu 22.04
- Ansible 2.10.8
- Vagrant et VirtualBox
- Nginx

## Fichiers du projet
- `inventory.ini` : inventaire des machines cibles
- `install-nginx.yml` : playbook d'installation et de configuration de Nginx

## Travaux realises
1. Creation d'un inventaire Ansible.
2. Test de connexion avec le module ping.
3. Creation d'un playbook YAML.
4. Installation automatique de Nginx.
5. Demarrage et activation du service Nginx.
6. Verification HTTP avec curl.
7. Test de l'idempotence.

## Resultats
- Connexion Ansible : SUCCESS
- Verification HTTP : 200 OK
- Premiere execution : changed=1, failed=0
- Deuxieme execution : changed=0, failed=0

## Competences mises en pratique
Ansible, YAML, Linux, automatisation, gestion des services, infrastructure et idempotence.
