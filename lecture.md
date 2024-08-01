# Partie 1


# Gestion des Vulnérabilités en Cybersécurité

- Référence : https://www.orangecyberdefense.com/fr/insights/blog/gestion-des-vulnerabilites/vulnerabilites-de-quoi-parle-t-on

# 1 - Processus de Gestion des Vulnérabilités

- La gestion des vulnérabilités est un processus fondamental en cybersécurité. Elle comprend plusieurs étapes cruciales pour garantir que les systèmes d'information restent sécurisés contre les cybermenaces. 

![image](https://github.com/hrhouma/prevention-securite-de-linformation/assets/10111526/91264a43-65d5-423b-979e-243fc6a893a9)


- Voici une description détaillée de chaque étape du processus.

1. **Découverte**
   - **Définition**: La découverte de vulnérabilités consiste à identifier les failles de sécurité potentielles dans les systèmes, les logiciels ou les composants matériels. Cette étape peut être effectuée par des équipes internes de sécurité, des chercheurs externes ou des sociétés spécialisées en cybersécurité.
   - **Méthodes**:
     - **Analyse de code**: Les outils d'analyse statique et dynamique permettent de détecter des erreurs dans le code source qui pourraient représenter des vulnérabilités.
     - **Tests de pénétration**: Les pentests simulent des attaques réelles pour identifier les points faibles du système.
     - **Audits de sécurité**: Les audits systématiques des configurations et des pratiques de sécurité peuvent révéler des vulnérabilités cachées.
     - **Bug Bounty**: Les programmes de bug bounty offrent des récompenses aux chercheurs indépendants qui découvrent et signalent des vulnérabilités.

2. **Rapport**
   - **Définition**: Une fois qu'une vulnérabilité est découverte, un rapport détaillé est créé. Ce rapport inclut des informations sur la nature de la vulnérabilité, son impact potentiel, et des recommandations pour sa correction.
   - **Contenu du rapport**:
     - **Description technique**: Une explication détaillée de la vulnérabilité, y compris où et comment elle se produit.
     - **Preuve de concept (PoC)**: Un exemple pratique montrant comment la vulnérabilité peut être exploitée.
     - **Impact**: Une évaluation des risques associés à la vulnérabilité, y compris les dommages potentiels.
     - **Recommandations**: Des suggestions pour corriger la vulnérabilité ou atténuer les risques.
   - **Envoi**: Le rapport est envoyé à l'éditeur du logiciel ou au responsable du composant vulnérable. Une date butoir pour la réponse est souvent incluse pour garantir une action rapide.

3. **Réception**
   - **Confirmation**: L'éditeur du logiciel ou le responsable reçoit le rapport et confirme la réception ainsi que la validité de la vulnérabilité. Cela peut nécessiter des discussions et des clarifications supplémentaires avec le chercheur.
   - **Planification**: L'éditeur planifie les étapes nécessaires pour corriger la vulnérabilité. Cela inclut la coordination avec les équipes de développement, de test et de déploiement.

4. **Correction**
   - **Développement de correctifs**: L'éditeur développe un correctif pour la vulnérabilité. Ce correctif peut être un patch temporaire ou une mise à jour complète du logiciel.
     - **Patches temporaires**: Utilisés pour corriger rapidement une vulnérabilité avant qu'une solution plus permanente ne soit disponible.
     - **Mises à jour de version**: Incluent souvent des correctifs pour plusieurs vulnérabilités ainsi que des améliorations de fonctionnalités.
   - **Tests de correctifs**: Avant le déploiement, les correctifs doivent être rigoureusement testés pour s'assurer qu'ils corrigent la vulnérabilité sans introduire de nouveaux problèmes.
   - **Communication**: L'éditeur informe le chercheur et les utilisateurs du correctif, en fournissant des instructions sur son application.

5. **Vérification**
   - **Validation**: Le chercheur qui a découvert la vulnérabilité vérifie que le correctif fonctionne comme prévu. Cette étape implique souvent de répéter les tests initiaux pour s'assurer que la vulnérabilité est bien corrigée.
   - **Tests supplémentaires**: Des tests supplémentaires peuvent être réalisés pour s'assurer que le correctif ne perturbe pas d'autres fonctionnalités du système et qu'il résout effectivement la vulnérabilité.

6. **Publication**
   - **Coordination**: Une fois le correctif validé, il y a une coordination entre le chercheur et l'éditeur pour publier les informations relatives à la vulnérabilité et au correctif. 
     - **Bulletins de sécurité**: Les bulletins de sécurité sont des annonces formelles publiées par les éditeurs pour informer les utilisateurs des vulnérabilités découvertes et des correctifs disponibles.
     - **Annonces publiques**: Des annonces peuvent être faites via des blogs, des forums de sécurité ou des médias sociaux pour atteindre une audience plus large.
   - **Sensibilisation**: La publication vise à sensibiliser les utilisateurs et les administrateurs de systèmes aux vulnérabilités et aux correctifs disponibles, afin de réduire les risques d'exploitation.
   - **Documentation**: Des guides détaillés et des instructions sur la manière d'appliquer les correctifs sont souvent fournis pour aider les utilisateurs à sécuriser leurs systèmes.

### Importance de la Gestion des Vulnérabilités

- **Prévention des Attaques**: En identifiant et en corrigeant rapidement les vulnérabilités, les organisations peuvent prévenir de nombreuses cyberattaques avant qu'elles ne surviennent.
- **Conformité Réglementaire**: De nombreuses régulations et standards de sécurité, comme le RGPD ou la norme ISO 27001, exigent une gestion proactive des vulnérabilités pour protéger les données sensibles et les systèmes critiques.
- **Réduction des Risques**: Une gestion efficace des vulnérabilités réduit la surface d'attaque des systèmes, minimisant ainsi les risques d'exploitation par des cybercriminels.
- **Protection de la Réputation**: La gestion proactive des vulnérabilités aide à maintenir la confiance des clients et des partenaires en montrant un engagement envers la sécurité.

### Conclusion

- La gestion des vulnérabilités est un processus continu et essentiel pour assurer la sécurité des systèmes d'information. En suivant les étapes de découverte, rapport, réception, correction, vérification et publication, les organisations peuvent renforcer leur posture de sécurité et protéger leurs actifs contre les cybermenaces potentielles. Ce processus nécessite une collaboration étroite entre les chercheurs en sécurité, les éditeurs de logiciels et les responsables de la sécurité informatique pour garantir une réponse rapide et efficace aux nouvelles vulnérabilités.

# 2 - Outils

### Exemple de Logiciels Utilisés dans Chaque Phase de Gestion des Vulnérabilités

| **Phase**            | **Logiciels**                                                                                               | **Description**                                                                                      |
|----------------------|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| **Découverte**       | - **Nessus**                                                                                                 | Un scanner de vulnérabilités qui identifie les failles de sécurité dans les systèmes et les réseaux.  |
|                      | - **OpenVAS**                                                                                               | Un outil open source pour la gestion et le scanning des vulnérabilités.                               |
|                      | - **Metasploit**                                                                                            | Un framework pour les tests de pénétration et l'exploitation de vulnérabilités.                       |
|                      | - **BeEF (Browser Exploitation Framework)**                                                                 | Un outil pour tester les vulnérabilités de sécurité des navigateurs web.                              |
|                      | - **Recon-ng**                                                                                              | Un outil de reconnaissance web écrit en Python.                                                      |
| **Rapport**          | - **Dradis**                                                                                                | Un outil de collaboration pour les tests de sécurité, facilitant la rédaction de rapports.            |
|                      | - **Faraday**                                                                                               | Une plateforme collaborative de tests de sécurité qui aide à centraliser les résultats des scans.     |
|                      | - **TheHive**                                                                                               | Une plateforme pour gérer les incidents de sécurité et les vulnérabilités avec des rapports détaillés. |
| **Réception**        | - **JIRA**                                                                                                  | Un outil de gestion de projet souvent utilisé pour suivre la réception et la correction des bugs.     |
|                      | - **ServiceNow**                                                                                            | Un outil de gestion des services informatiques pour gérer les incidents et les vulnérabilités.        |
|                      | - **Zendesk**                                                                                               | Un logiciel de support client qui peut être utilisé pour gérer les tickets de vulnérabilités.         |
| **Correction**       | - **Patch Management Tools (ex: WSUS, SCCM)**                                                               | Des outils de gestion de correctifs pour déployer des mises à jour de sécurité sur les systèmes.      |
|                      | - **Chef, Puppet, Ansible**                                                                                 | Des outils de gestion de configuration pour automatiser le déploiement des correctifs.                |
|                      | - **Qualys Patch Management**                                                                               | Une solution cloud pour gérer les correctifs de sécurité.                                             |
| **Vérification**     | - **Retest avec Nessus, OpenVAS**                                                                           | Utilisation de scanners pour vérifier que les correctifs ont bien été appliqués.                      |
|                      | - **Burp Suite**                                                                                            | Un outil de test de sécurité des applications web pour vérifier les correctifs appliqués.             |
|                      | - **Nmap**                                                                                                  | Un scanner réseau pour vérifier que les vulnérabilités ont été corrigées et les ports sécurisés.      |
| **Publication**      | - **Wiki.js**                                                                                               | Un système de gestion de contenu open source pour documenter et publier les informations de sécurité. |
|                      | - **Security Advisories (ex: Microsoft Security Bulletins)**                                                | Publications formelles des correctifs et des informations sur les vulnérabilités.                     |
|                      | - **Exploit Database**                                                                                      | Une base de données en ligne des vulnérabilités et des exploits publiés.                              |
|                      | - **Full Disclosure Mailing List**                                                                          | Une liste de diffusion pour la divulgation publique des vulnérabilités.                               |

### Détails des Logiciels Utilisés

#### Découverte
- **Nessus** : Un scanner de vulnérabilités commercial qui offre une analyse approfondie des systèmes et réseaux pour identifier les failles de sécurité.
- **OpenVAS** : Un outil open source pour la gestion des vulnérabilités, capable de scanner et d'identifier les failles dans divers systèmes.
- **Metasploit** : Utilisé pour les tests de pénétration, il permet de simuler des attaques réelles pour identifier les points faibles.
- **BeEF** : Spécialisé dans l'exploitation des failles des navigateurs, cet outil est utilisé pour tester la sécurité des applications web.
- **Recon-ng** : Un outil de reconnaissance et de collecte d'informations sur les cibles potentielles.

#### Rapport
- **Dradis** : Facilite la collaboration entre les équipes de sécurité en centralisant les informations sur les tests de sécurité et les résultats des scans.
- **Faraday** : Une plateforme qui permet de centraliser les résultats des tests de sécurité et de faciliter la collaboration entre les équipes.
- **TheHive** : Utilisé pour gérer les incidents de sécurité, cet outil permet de générer des rapports détaillés sur les vulnérabilités découvertes.

#### Réception
- **JIRA** : Utilisé pour suivre les problèmes et les bugs, il permet aux équipes de sécurité de gérer la réception et la correction des vulnérabilités.
- **ServiceNow** : Offre des fonctionnalités de gestion des services informatiques, y compris la gestion des incidents de sécurité.
- **Zendesk** : Utilisé pour la gestion des tickets, il permet de suivre et de gérer les rapports de vulnérabilités.

#### Correction
- **WSUS, SCCM** : Outils de Microsoft pour la gestion des mises à jour et des correctifs de sécurité.
- **Chef, Puppet, Ansible** : Outils de gestion de configuration qui automatisent le déploiement des correctifs de sécurité.
- **Qualys Patch Management** : Une solution cloud pour gérer et déployer les correctifs de sécurité.

#### Vérification
- **Nessus, OpenVAS** : Utilisés pour rescaner les systèmes après l'application des correctifs afin de vérifier leur efficacité.
- **Burp Suite** : Un outil de test de sécurité des applications web pour s'assurer que les vulnérabilités ont été correctement corrigées.
- **Nmap** : Utilisé pour vérifier les configurations réseau et s'assurer que les correctifs de sécurité ont été appliqués correctement.

#### Publication
- **Wiki.js** : Un système de gestion de contenu open source pour documenter et publier les informations de sécurité. Il permet de créer une base de connaissances structurée et facilement accessible.
- **Security Advisories** : Les bulletins de sécurité publiés par les éditeurs pour informer les utilisateurs des vulnérabilités et des correctifs.
- **Exploit Database** : Une base de données en ligne où les vulnérabilités et les exploits sont publiés.
- **Full Disclosure Mailing List** : Une liste de diffusion où les chercheurs et les éditeurs peuvent publier des informations sur les vulnérabilités découvertes et corrigées.

- Ce tableau et ces descriptions montrent comment différents logiciels et outils sont utilisés à chaque étape de la gestion des vulnérabilités pour assurer la sécurité des systèmes d'information. Wiki.js, en particulier, est un excellent outil pour centraliser et publier des informations sur les vulnérabilités et les correctifs, offrant ainsi une ressource précieuse pour les équipes de sécurité et les utilisateurs.

# Références :
- https://www.orangecyberdefense.com/fr/insights/blog/gestion-des-vulnerabilites/vulnerabilites-de-quoi-parle-t-on
- https://www.geeksforgeeks.org/recon-ng-installation-on-kali-linux/
- https://www.javatpoint.com/recon-ng-information-gathering-tool-in-kali-linux
- https://www.kali.org/tools/recon-ng/
- https://manpages.ubuntu.com/manpages/bionic/man1/recon-ng.1.html
- https://www.kali.org/docs/introduction/should-i-use-kali-linux/
- https://medium.com/@Infosec-Train/why-do-hackers-use-kali-linux5217e95e7a97#:~:text=Hackers%20use%20Kali%20Linux%20as,hacking%20for%20the%20first%20time.
- https://www.orangecyberdefense.com/fr/insights/blog/gestion-des-vulnerabilites/vulnerabilites-de-quoi-parle-t-on
- https://www.linkedin.com/pulse/cyber-s%C3%A9curit%C3%A9-les-diff%C3%A9rentes-%C3%A9tapes-dune-attaque-franque-tsue/
- https://www.netscout.com/ddos-attack-map
- https://cybermap.kaspersky.com/fr
- https://unix.stackexchange.com/questions/244970/opening-current-directory-from-a-terminal-onto-a-file-browser

-----
# Partie 2


# 1 - Les Étapes d'une Attaque Informatique

Les cyberattaques sont devenues une menace omniprésente pour les entreprises et les organisations de toutes tailles. Comprendre les différentes étapes d'une attaque informatique est crucial pour renforcer les défenses et protéger les systèmes d'information contre les intrusions. Une attaque informatique typique se déroule généralement en cinq étapes : récolte des informations, identification des vulnérabilités, exploitation des failles, maintien de l'intrusion, et effacement des traces. Cet article explore ces étapes en détail pour aider les responsables de la sécurité à mieux comprendre et anticiper les menaces potentielles.

### 1. Récolte des Informations

#### Informations Techniques et Sociales

Les attaquants commencent par une phase de reconnaissance pour recueillir autant d'informations que possible sur la cible. Cela peut inclure des données techniques, telles que les adresses IP des serveurs accessibles de l'extérieur (comme les serveurs web et de messagerie), ainsi que les services disponibles sur ces serveurs. Ils dressent ainsi une cartographie du système d'information. 

En parallèle, les attaquants exploitent des informations sociales obtenues par ingénierie sociale, en ciblant les employés de l'entreprise, les prestataires, et les services. Par exemple, ils peuvent utiliser les réseaux sociaux pour identifier les membres de l'organisation et les informations qu'ils partagent publiquement, comme leurs rôles, leurs coordonnées, et leurs habitudes de travail. L'objectif est de trouver des points d'entrée et des vulnérabilités humaines.

#### Méthodes de Récolte

- **Récolte Passive** : Cette méthode consiste à recueillir des informations sans interagir directement avec le système cible, ce qui la rend discrète et difficile à détecter. Les attaquants utilisent des moteurs de recherche pour trouver des informations publiques sur la cible, des bases de données accessibles (comme celles contenant des informations sur les noms de domaine), et les réseaux sociaux pour obtenir des données personnelles sur les employés.

  Par exemple, un attaquant peut utiliser des outils comme Shodan pour scanner des adresses IP à la recherche de services et de systèmes exposés. Ils peuvent également consulter les archives de sites web comme Archive.org pour obtenir des versions précédentes de sites web, qui peuvent contenir des informations précieuses sur l'infrastructure de l'entreprise.

- **Récolte Active** : Cette méthode implique l'utilisation d'outils spécifiques pour interroger directement la cible. Bien que plus efficace, cette méthode est moins discrète et peut être détectée par les systèmes de sécurité de l'entreprise. Les attaquants peuvent utiliser des outils comme Nmap pour scanner les ports ouverts et les services actifs sur les serveurs de l'entreprise, ou lancer des attaques de phishing pour obtenir des informations d'identification.

  Par exemple, un attaquant peut envoyer des courriels de phishing ciblés à des employés spécifiques, contenant des liens vers des sites web factices conçus pour capturer leurs informations de connexion. Ils peuvent également utiliser des malwares pour infecter les systèmes et recueillir des informations directement à partir de l'intérieur du réseau.

### 2. Identification des Vulnérabilités

Une fois les informations recueillies, les attaquants passent à l'analyse de ces données pour identifier les vulnérabilités exploitables. Cette phase est cruciale car elle permet de déterminer les points faibles du système cible et d'évaluer les chances de succès de l'attaque.

#### Types de Vulnérabilités

Les vulnérabilités peuvent être de nature technique ou non technique, et elles affectent la confidentialité, l'intégrité, et la disponibilité des systèmes d'information.

- **Failles Techniques** : Ce sont des faiblesses dans le système lui-même, telles que des configurations de serveur incorrectes, des systèmes d'exploitation non mis à jour, ou des failles dans les applications. Par exemple, une mauvaise configuration de serveur pourrait permettre à un attaquant d'accéder à des fichiers sensibles ou de prendre le contrôle du serveur.

  Un exemple courant de faille technique est la vulnérabilité de type SQL injection, où un attaquant peut injecter du code malveillant dans une requête SQL pour accéder à la base de données et manipuler ou voler des données.

- **Failles Non Techniques** : Ces failles sont liées aux comportements humains et aux processus organisationnels. Elles incluent des mots de passe faibles, des droits d'utilisateur trop permissifs, et des pratiques de sécurité inadéquates. Par exemple, un employé utilisant un mot de passe simple et facile à deviner expose l'entreprise à un risque élevé d'intrusion.

  Un exemple de faille non technique est l'ingénierie sociale, où un attaquant manipule les employés pour obtenir des informations confidentielles. Par exemple, un attaquant pourrait se faire passer pour un membre du service informatique et demander des informations de connexion sous prétexte de maintenance.

#### Évaluation des Vulnérabilités

Les attaquants utilisent divers outils pour identifier et évaluer les vulnérabilités. Des scanners de vulnérabilités comme Nessus ou OpenVAS peuvent être utilisés pour analyser les systèmes et identifier les failles. Les résultats de ces analyses permettent aux attaquants de planifier leurs attaques en fonction des faiblesses découvertes.

### 3. Exploitation des Failles

Une fois les vulnérabilités identifiées, les attaquants passent à l'exécution de l'attaque. L'exploitation des failles peut prendre différentes formes, selon la nature de la vulnérabilité et les objectifs de l'attaquant.

#### Types d'Exploitation

- **Injection de Code Malveillant** : Les attaquants peuvent injecter du code malveillant dans les applications ou les systèmes d'exploitation vulnérables pour en prendre le contrôle. Par exemple, une vulnérabilité de type buffer overflow peut être exploitée pour exécuter du code arbitraire sur le système cible.

  Un exemple courant est l'exploitation des failles de type XSS (cross-site scripting) dans les applications web, où un attaquant injecte du code JavaScript malveillant pour voler des cookies de session ou rediriger les utilisateurs vers des sites malveillants.

- **Attaques par Déni de Service (DDoS)** : Les attaquants peuvent viser la disponibilité des systèmes en lançant des attaques par déni de service, qui saturent les ressources du système cible et le rendent inaccessible. Par exemple, une attaque DDoS peut inonder un serveur web de requêtes, le faisant planter et empêchant les utilisateurs légitimes d'accéder au site.

  Un exemple est l'utilisation de botnets, où un grand nombre de dispositifs compromis sont utilisés pour envoyer un volume massif de trafic vers le système cible, le rendant indisponible.

- **Vol d'Informations** : Les attaquants peuvent voler des informations sensibles en exploitant des vulnérabilités dans les bases de données ou en utilisant l'ingénierie sociale. Par exemple, une base de données vulnérable peut permettre à un attaquant d'extraire des informations personnelles ou financières.

  Un exemple est l'attaque sur Equifax en 2017, où des attaquants ont exploité une vulnérabilité dans une application web pour accéder à des informations personnelles de plus de 140 millions de personnes.

### 4. Maintien de l'Intrusion

Après avoir réussi à s'introduire dans le système, l'attaquant cherche à maintenir son accès pour de futures actions malveillantes. Cette étape est essentielle pour garantir que l'attaquant puisse revenir dans le système sans être détecté.

#### Techniques de Maintien

- **Porte Dérobée (Backdoor)** : Les attaquants installent des malwares ou des rootkits qui permettent un accès continu et discret au système. Ces portes dérobées sont conçues pour se lancer automatiquement à chaque démarrage du système, garantissant ainsi un accès persistant.

  Par exemple, un attaquant peut utiliser un rootkit pour modifier le noyau du système d'exploitation et masquer la présence du malware, rendant sa détection extrêmement difficile.

- **Élévation des Privilèges** : L'attaquant cherche à obtenir des droits élevés sur le système pour exécuter des actions administratives. Cela peut impliquer l'exploitation de vulnérabilités supplémentaires pour obtenir un accès root ou administrateur.

  Un exemple est l'utilisation d'une attaque de type privilege escalation, où un attaquant utilise des failles dans le système pour obtenir des droits plus élevés que ceux initialement obtenus.

- **Déplacement Horizontal** : Une fois dans le système, l'attaquant explore le réseau interne pour accéder à d'autres systèmes et ressources. Cela permet à l'attaquant d'étendre son contrôle et de compromettre davantage d'éléments du réseau.

  Par exemple, un attaquant qui a compromis un poste de travail peut utiliser des outils comme Mimikatz pour voler des informations d'identification et accéder à d'autres systèmes sur le réseau.

### 5. Effacement des Traces

Pour éviter d'être détecté et pour compliquer les efforts de remédiation, l'attaquant efface toutes les traces de son intrusion. Cette étape est cruciale pour assurer l'anonymat de l'attaquant et pour prolonger la durée de l'intrusion.

#### Techniques d'Effacement

- **Effacement des Fichiers Journaux** : L'attaquant supprime ou modifie les journaux d'événements du système pour éliminer les preuves de son activité. Les journaux d'événements contiennent des enregistrements de toutes les actions effectuées sur le système, et leur manipulation permet de masquer l'intrusion.

  Par exemple, un attaquant peut utiliser des scripts pour automatiser la suppression ou la falsification des logs,

 rendant son activité indétectable.

- **Falsification des Fichiers Journaux** : En plus de supprimer les logs, l'attaquant peut les falsifier pour créer de fausses pistes et détourner l'attention des enquêteurs. Cela complique l'analyse forensique et rend plus difficile l'identification de l'attaquant.

  Un exemple est l'utilisation d'outils pour modifier les horodatages et les contenus des logs, créant ainsi une fausse chronologie des événements.

- **Anonymisation en Amont** : Avant même de lancer l'attaque, l'attaquant prend des mesures pour anonymiser ses actions, comme l'utilisation de VPN, de proxies, et de services anonymes pour masquer son adresse IP et ses traces numériques.

  Par exemple, un attaquant peut utiliser le réseau Tor pour masquer son emplacement et rendre plus difficile la traçabilité de ses actions.

### Conclusion

Une cyberattaque ne se limite pas à l'intrusion initiale, mais englobe l'ensemble des étapes de préparation, d'exécution, et de dissimulation. Comprendre ces étapes permet aux responsables de la sécurité de mieux anticiper et prévenir les attaques. En identifiant et en corrigeant les vulnérabilités, en surveillant les systèmes pour détecter les activités suspectes, et en mettant en place des mesures de sécurité robustes, les organisations peuvent se protéger efficacement contre les cyberattaques. Une analyse régulière des risques et des vulnérabilités est essentielle pour maintenir un haut niveau de sécurité et pour prévenir les intrusions.


# 2 -  (Les Logiciels Utilisés) - Étapes d'une Attaque Informatique et 

| Phase                        | Description                                                                                                                                                                     | Exemples de Logiciels Utilisés                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| **Récolte des Informations** | **Informations Techniques et Sociales** : Collecte des données sur la cible par des moyens passifs et actifs.                                                                   | Nmap, Recon-ng, Shodan, Maltego, theHarvester, FOCA, SpiderFoot        |
|                              | **Méthodes de Récolte Passive** : Utilisation de moteurs de recherche, bases de données et réseaux sociaux pour obtenir des informations.                                      | Google Dorks, LinkedIn, Facebook, Whois, DNSDumpster                   |
|                              | **Méthodes de Récolte Active** : Utilisation d'outils spécifiques pour interroger directement la cible.                                                                        | Nmap, Nessus, OpenVAS, Nikto, Metasploit                               |
| **Identification des Vulnérabilités** | Analyse des informations collectées pour trouver des failles exploitables.                                                                                                          | Nessus, OpenVAS, Nexpose, Burp Suite, ZAP, Acunetix, SQLMap            |
| **Exploitation des Failles** | **Injection de Code Malveillant** : Utilisation de vulnérabilités pour exécuter du code malveillant sur la cible.                                                              | Metasploit, SQLMap, BeEF, ExploitDB, Commix, XSSer                     |
|                              | **Attaques par Déni de Service (DDoS)** : Saturation des ressources du système cible pour le rendre inaccessible.                                                               | LOIC, HOIC, Slowloris, Hping, DDoS-Guard, PyLoris                      |
|                              | **Vol d'Informations** : Exploitation des failles pour accéder et voler des informations sensibles.                                                                            | SQLMap, Hydra, John the Ripper, Wireshark, Aircrack-ng                 |
| **Maintien de l'Intrusion**  | **Porte Dérobée (Backdoor)** : Installation de malwares pour un accès continu et discret.                                                                                      | Metasploit, Netcat, Empire, Cobalt Strike, Mimikatz                    |
|                              | **Élévation des Privilèges** : Exploitation des vulnérabilités pour obtenir des droits administratifs.                                                                         | Metasploit, Mimikatz, PowerSploit, Dirty COW, WinPwn                   |
|                              | **Déplacement Horizontal** : Exploration du réseau interne pour compromettre d'autres systèmes.                                                                               | BloodHound, CrackMapExec, Responder, Impacket, smbclient               |
| **Effacement des Traces**    | **Effacement des Fichiers Journaux** : Suppression ou modification des logs pour éliminer les preuves.                                                                        | Metasploit, CCleaner, BleachBit, Log Cleaner, PowerShell scripts       |
|                              | **Falsification des Fichiers Journaux** : Modification des logs pour créer de fausses pistes.                                                                                  | Metasploit, Auditpol, EventLog Explorer, Klog                          |
|                              | **Anonymisation en Amont** : Utilisation de techniques pour rester anonyme et masquer les traces numériques.                                                                  | Tor, VPNs, ProxyChains, Whonix, Tails                                  |

### Description des Logiciels

1. **Nmap** : Outil de scan réseau pour découvrir les hôtes et services sur un réseau.
2. **Recon-ng** : Cadre de reconnaissance web écrit en Python, conçu pour effectuer des tâches de reconnaissance web de manière efficace et modulaire.
3. **Shodan** : Moteur de recherche pour trouver des appareils connectés à l'internet.
4. **Maltego** : Outil d'analyse de données et de cartographie de réseau qui permet de relier et de visualiser des informations provenant de diverses sources.
5. **theHarvester** : Outil de collecte d'e-mails, de noms d'utilisateurs et d'informations d'hôte ou de domaine à partir de différentes sources publiques.
6. **FOCA** : Outil de collecte d'informations et de métadonnées à partir de documents et de fichiers trouvés en ligne.
7. **SpiderFoot** : Outil d'automatisation de reconnaissance qui collecte des informations sur les cibles à partir de sources ouvertes.
8. **Google Dorks** : Techniques de recherche avancées utilisant Google pour trouver des informations sensibles.
9. **LinkedIn, Facebook** : Réseaux sociaux utilisés pour la reconnaissance sociale.
10. **Whois** : Outil de recherche d'informations sur les noms de domaine.
11. **DNSDumpster** : Outil de reconnaissance DNS.
12. **Nessus, OpenVAS, Nexpose** : Scanners de vulnérabilités pour identifier les failles dans les systèmes et applications.
13. **Burp Suite, ZAP** : Outils d'analyse et de test de sécurité pour les applications web.
14. **Acunetix** : Scanner de vulnérabilités web automatisé.
15. **SQLMap** : Outil d'automatisation de tests d'injections SQL.
16. **BeEF** : Framework pour tester les vulnérabilités XSS.
17. **ExploitDB** : Base de données d'exploits connus et de proof-of-concepts.
18. **Commix** : Outil d'exploitation des injections de commandes dans les applications web.
19. **XSSer** : Outil d'exploitation des vulnérabilités de type XSS.
20. **LOIC, HOIC** : Outils pour lancer des attaques par déni de service.
21. **Slowloris** : Outil pour lancer des attaques DoS en gardant les connexions ouvertes sur un serveur.
22. **Hping** : Outil de génération de paquets TCP/IP pour des tests et des attaques réseau.
23. **DDoS-Guard** : Outil pour protéger contre les attaques DDoS.
24. **PyLoris** : Outil pour lancer des attaques DoS sur les services web.
25. **Hydra** : Outil de force brute pour casser les mots de passe.
26. **John the Ripper** : Outil de cassage de mots de passe.
27. **Wireshark** : Analyseur de paquets réseau.
28. **Aircrack-ng** : Suite d'outils pour évaluer la sécurité des réseaux Wi-Fi.
29. **Netcat** : Outil pour lire et écrire des données sur les connexions réseau.
30. **Empire** : Framework de post-exploitation pour Windows et Unix.
31. **Cobalt Strike** : Outil de red teaming pour la simulation d'attaques avancées.
32. **Mimikatz** : Outil pour extraire des informations d'identification en mémoire sur Windows.
33. **PowerSploit** : Collection de modules PowerShell utilisés pour les tests d'intrusion.
34. **Dirty COW** : Exploit de type privilege escalation pour Linux.
35. **WinPwn** : Collection d'outils et de scripts pour l'exploitation de Windows.
36. **BloodHound** : Outil d'analyse Active Directory pour trouver les chemins d'attaque dans les réseaux Windows.
37. **CrackMapExec** : Outil de post-exploitation pour automatiser les tests Active Directory.
38. **Responder** : Outil pour la capture de noms d'utilisateur et de mots de passe sur un réseau local.
39. **Impacket** : Collection de scripts Python pour la manipulation des protocoles réseau.
40. **smbclient** : Outil pour interagir avec les partages de fichiers SMB/CIFS.
41. **CCleaner, BleachBit** : Outils de nettoyage des fichiers et des traces sur les systèmes d'exploitation.
42. **Log Cleaner** : Outil pour nettoyer les fichiers journaux.
43. **PowerShell scripts** : Scripts pour automatiser les tâches d'effacement et de modification des logs.
44. **Auditpol** : Utilitaire Windows pour la gestion des politiques d'audit.
45. **EventLog Explorer** : Outil pour visualiser et manipuler les logs Windows.
46. **Klog** : Outil pour la gestion et la manipulation des logs.
47. **Tor** : Réseau pour naviguer anonymement sur Internet.
48. **VPNs** : Réseaux privés virtuels pour masquer l'adresse IP.
49. **ProxyChains** : Outil pour enchaîner les connexions via plusieurs proxys.
50. **Whonix, Tails** : Systèmes d'exploitation conçus pour la sécurité et l'anonymat.


# 3 - Annexe - Logiciels Utilisés pour Chaque Phase d'une Attaque Informatique

#### Phase 1: Récolte des Informations

**Récolte Passive :**

1. **Google Dorks**: Techniques avancées de recherche sur Google pour trouver des informations sensibles.
2. **LinkedIn, Facebook**: Utilisés pour collecter des informations sociales et professionnelles.
3. **Whois**: Recherche d'informations sur les noms de domaine et les propriétaires.
4. **DNSDumpster**: Outil de reconnaissance DNS pour cartographier l'infrastructure d'un domaine.
5. **FOCA**: Analyse les documents pour extraire les métadonnées.

**Récolte Active :**

1. **Nmap**: Outil de scan réseau pour découvrir les hôtes et services.
2. **Nessus**: Scanner de vulnérabilités pour identifier les failles dans les systèmes.
3. **OpenVAS**: Système avancé de scan de vulnérabilités.
4. **Metasploit**: Framework pour tester les exploits et les vulnérabilités.
5. **Recon-ng**: Cadre de reconnaissance web pour automatiser la collecte de données.

#### Phase 2: Identification des Vulnérabilités

1. **Nessus**: Identifie les vulnérabilités à partir des informations collectées.
2. **OpenVAS**: Scanner de vulnérabilités open-source.
3. **Nexpose**: Plateforme de gestion de vulnérabilités.
4. **Burp Suite**: Outil de test de sécurité des applications web.
5. **ZAP (Zed Attack Proxy)**: Scanner de vulnérabilités pour les applications web.
6. **Acunetix**: Scanner de vulnérabilités web automatisé.
7. **SQLMap**: Outil d'automatisation des tests d'injections SQL.
8. **BeEF (Browser Exploitation Framework)**: Framework pour tester les vulnérabilités XSS.

#### Phase 3: Exploitation des Failles

**Injection de Code Malveillant :**

1. **Metasploit**: Exploite les vulnérabilités pour exécuter du code malveillant.
2. **SQLMap**: Utilisé pour exploiter les injections SQL.
3. **BeEF**: Exploite les vulnérabilités XSS dans les navigateurs.
4. **Commix**: Outil pour l'injection de commandes dans les applications web.
5. **XSSer**: Automatisation des attaques XSS.

**Attaques par Déni de Service (DDoS) :**

1. **LOIC (Low Orbit Ion Cannon)**: Outil pour lancer des attaques DDoS.
2. **HOIC (High Orbit Ion Cannon)**: Outil DDoS avancé.
3. **Slowloris**: Attaque DoS qui garde les connexions ouvertes sur un serveur.
4. **Hping**: Générateur de paquets TCP/IP pour des tests réseau.
5. **PyLoris**: Outil DDoS pour les services web.

**Vol d'Informations :**

1. **Hydra**: Outil de force brute pour casser les mots de passe.
2. **John the Ripper**: Outil pour casser les mots de passe.
3. **Wireshark**: Analyseur de paquets réseau.
4. **Aircrack-ng**: Suite d'outils pour évaluer la sécurité des réseaux Wi-Fi.

#### Phase 4: Maintien de l'Intrusion

**Porte Dérobée (Backdoor) :**

1. **Netcat**: Outil pour lire et écrire des données sur les connexions réseau.
2. **Empire**: Framework de post-exploitation pour Windows et Unix.
3. **Cobalt Strike**: Outil de red teaming pour simuler des attaques avancées.
4. **Mimikatz**: Extraction d'informations d'identification en mémoire.
5. **Metasploit**: Installation de portes dérobées.

**Élévation des Privilèges :**

1. **Mimikatz**: Élévation des privilèges sur les systèmes Windows.
2. **PowerSploit**: Collection de modules PowerShell pour les tests d'intrusion.
3. **Dirty COW**: Exploit de type privilege escalation pour Linux.
4. **WinPwn**: Scripts pour l'exploitation de Windows.

**Déplacement Horizontal :**

1. **BloodHound**: Analyse Active Directory pour trouver des chemins d'attaque.
2. **CrackMapExec**: Automatisation des tests Active Directory.
3. **Responder**: Capture des noms d'utilisateur et des mots de passe sur un réseau.
4. **Impacket**: Scripts pour la manipulation des protocoles réseau.
5. **smbclient**: Interagir avec les partages de fichiers SMB/CIFS.

#### Phase 5: Effacement des Traces

**Effacement des Fichiers Journaux :**

1. **CCleaner**: Nettoyage des fichiers et des traces sur les systèmes.
2. **BleachBit**: Outil de nettoyage des fichiers.
3. **Log Cleaner**: Nettoyage des fichiers journaux.
4. **Metasploit**: Modules pour effacer les traces.

**Falsification des Fichiers Journaux :**

1. **Auditpol**: Gestion des politiques d'audit sur Windows.
2. **EventLog Explorer**: Visualisation et manipulation des logs Windows.
3. **Klog**: Outil pour gérer et falsifier les logs.

**Anonymisation en Amont :**

1. **Tor**: Réseau pour naviguer anonymement.
2. **VPNs**: Réseaux privés virtuels pour masquer l'adresse IP.
3. **ProxyChains**: Chainer les connexions via plusieurs proxys.
4. **Whonix**: Système d'exploitation pour la sécurité et l'anonymat.
5. **Tails**: Système d'exploitation conçu pour la sécurité et l'anonymat.

- Cette table résume les logiciels couramment utilisés à chaque étape d'une cyberattaque, offrant ainsi un aperçu des outils disponibles pour les attaquants et des moyens de défense possibles pour les responsables de la sécurité.
