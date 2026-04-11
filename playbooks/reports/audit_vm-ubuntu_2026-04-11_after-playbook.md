# 🛡️ Rapport d'Audit de Sécurité
> **Guide de référence :** ANSSI BP-028
> **Généré le :** 2026-04-11T20:11:50Z

## 📊 Résumé de la Conformité

| Paramètre | Valeur |
| :--- | :--- |
| **Machine** | `vm-ubuntu` |
| **OS** | Ubuntu 24.04 |
| **Score Final** | # 100.0 % |

---

## 📝 Détails des points de contrôle

| Statut | Point de Contrôle | Valeur Réelle | Attendu |
| :---: | :--- | :---: | :---: |
| ✅ | **[SYS] ASLR (randomize_va_space)** | `2` | `2` |
| ✅ | **[SYS] Buffer dmesg restreint** | `1` | `1` |
| ✅ | **[SYS] Masquage adresses noyau (kptr_restrict)** | `2` | `2` |
| ✅ | **[SYS] Restriction PTRACE (Yama)** | `1` | `1` |
| ✅ | **[SYS] BPF non privilégié désactivé** | `1` | `1` |
| ✅ | **[USR] Compte root verrouillé** | `OK` | `OK` |
| ✅ | **[USR] Shell du compte daemon** | `/usr/sbin/nologin` | `/usr/sbin/nologin` |
| ✅ | **[USR] Expiration des sessions (TMOUT)** | `OK` | `OK` |
| ✅ | **[FIC] Umask Global** | `027` | `027` |
| ✅ | **[FIC] Droits sur /etc/shadow** | `640 root shadow` | `640 root shadow` |
| ✅ | **[FIC] Protection liens symboliques** | `1` | `1` |
| ✅ | **[FIC] Sticky bit sur /tmp** | `1777` | `1777` |
| ✅ | **[FIC] /dev/shm (noexec)** | `OK` | `OK` |
| ✅ | **[NET] Désactivation IPv6** | `1` | `1` |
| ✅ | **[NET] Anti-spoofing (rp_filter)** | `1` | `1` |
| ✅ | **[NET] Accès Root SSH** | `no` | `no` |
| ✅ | **[NET] Statut Pare-feu UFW** | `active` | `active` |
| ✅ | **[PKG] Paquet vulnérable (nis) absent** | `OK` | `OK` |
| ✅ | **[PKG] Outils auto-upgrades présents** | `installed` | `installed` |
| ✅ | **[PKG] Correctifs de sécurité automatisés** | `OK` | `OK` |

---

## 🔍 Analyse détaillée par point

### ✅ [SYS] ASLR (randomize_va_space)
- **Description :** Mémoire imprévisible (ASLR) activée.
- **Résultat obtenu :** `2`
- **Conformité :** Conforme


---
### ✅ [SYS] Buffer dmesg restreint
- **Description :** Empêche les utilisateurs de lire les logs kernel.
- **Résultat obtenu :** `1`
- **Conformité :** Conforme


---
### ✅ [SYS] Masquage adresses noyau (kptr_restrict)
- **Description :** Cache les adresses mémoire du noyau.
- **Résultat obtenu :** `2`
- **Conformité :** Conforme


---
### ✅ [SYS] Restriction PTRACE (Yama)
- **Description :** Empêche l'espionnage entre processus locaux.
- **Résultat obtenu :** `1`
- **Conformité :** Conforme


---
### ✅ [SYS] BPF non privilégié désactivé
- **Description :** Restreint l'usage réseau bas niveau aux admins.
- **Résultat obtenu :** `1`
- **Conformité :** Conforme


---
### ✅ [USR] Compte root verrouillé
- **Description :** Le mot de passe root est désactivé (imputabilité sudo).
- **Résultat obtenu :** `OK`
- **Conformité :** Conforme


---
### ✅ [USR] Shell du compte daemon
- **Description :** Désactivation de la connexion pour le compte de service daemon.
- **Résultat obtenu :** `/usr/sbin/nologin`
- **Conformité :** Conforme


---
### ✅ [USR] Expiration des sessions (TMOUT)
- **Description :** Déconnexion automatique après 15 minutes d'inactivité.
- **Résultat obtenu :** `OK`
- **Conformité :** Conforme


---
### ✅ [FIC] Umask Global
- **Description :** Fichiers inaccessibles aux autres utilisateurs par défaut.
- **Résultat obtenu :** `027`
- **Conformité :** Conforme


---
### ✅ [FIC] Droits sur /etc/shadow
- **Description :** Fichier de mots de passe protégé en lecture.
- **Résultat obtenu :** `640 root shadow`
- **Conformité :** Conforme


---
### ✅ [FIC] Protection liens symboliques
- **Description :** Prévention contre les attaques par liens dans /tmp.
- **Résultat obtenu :** `1`
- **Conformité :** Conforme


---
### ✅ [FIC] Sticky bit sur /tmp
- **Description :** Seul le propriétaire peut supprimer son fichier dans /tmp.
- **Résultat obtenu :** `1777`
- **Conformité :** Conforme


---
### ✅ [FIC] /dev/shm (noexec)
- **Description :** Interdiction d'exécuter des scripts en mémoire RAM.
- **Résultat obtenu :** `OK`
- **Conformité :** Conforme


---
### ✅ [NET] Désactivation IPv6
- **Description :** Surface d'attaque IPv6 fermée.
- **Résultat obtenu :** `1`
- **Conformité :** Conforme


---
### ✅ [NET] Anti-spoofing (rp_filter)
- **Description :** Vérification stricte de l'origine des paquets IP.
- **Résultat obtenu :** `1`
- **Conformité :** Conforme


---
### ✅ [NET] Accès Root SSH
- **Description :** Connexion SSH en tant que root interdite.
- **Résultat obtenu :** `no`
- **Conformité :** Conforme


---
### ✅ [NET] Statut Pare-feu UFW
- **Description :** Pare-feu UFW allumé.
- **Résultat obtenu :** `active`
- **Conformité :** Conforme


---
### ✅ [PKG] Paquet vulnérable (nis) absent
- **Description :** Le service obsolète NIS n'est pas installé.
- **Résultat obtenu :** `OK`
- **Conformité :** Conforme


---
### ✅ [PKG] Outils auto-upgrades présents
- **Description :** Le gestionnaire de mises à jour de sécurité est installé.
- **Résultat obtenu :** `installed`
- **Conformité :** Conforme


---
### ✅ [PKG] Correctifs de sécurité automatisés
- **Description :** Téléchargement et installation automatique des patchs APT.
- **Résultat obtenu :** `OK`
- **Conformité :** Conforme


---

_Rapport généré automatiquement par Ansible_