### **Gestion des Permissions**

#### **1. Connexion en tant que Superutilisateur**
```bash
su
# Entrez le mot de passe du superutilisateur
```

#### **2. Création des Utilisateurs**
```bash
# Assurez-vous que les utilisateurs existent ou créez-les
useradd -m albert
useradd -m bernard
useradd -m claude
useradd -m danielle
```

#### **3. Création du Dossier et des Fichiers**
```bash
# Créer le dossier shared_data et les sous-dossiers/fichiers nécessaires
mkdir -p /home/shared_data
mkdir -p /home/shared_data/dossier1

touch /home/shared_data/file1.txt
touch /home/shared_data/file2.txt
touch /home/shared_data/dossier1/script1.sh
touch /home/shared_data/dossier1/script2.sh
```

#### **4. Attribution des Propriétaires et des Permissions**
```bash
# Configuration initiale des permissions et propriétaires
chown albert:albert /home/shared_data/file1.txt
chmod 644 /home/shared_data/file1.txt
chown albert:albert /home/shared_data/file2.txt
chmod 444 /home/shared_data/file2.txt

chown bernard:bernard /home/shared_data/file2.txt
chmod 664 /home/shared_data/file2.txt
chown bernard:bernard /home/shared_data/dossier1/script1.sh
chmod 751 /home/shared_data/dossier1/script1.sh

chown -R claude:claude /home/shared_data/dossier1
chmod 766 /home/shared_data/dossier1
chmod 666 /home/shared_data/dossier1/script1.sh
chmod 666 /home/shared_data/dossier1/script2.sh

chown -R danielle:danielle /home/shared_data
chmod -R 777 /home/shared_data
```

#### **5. Vérification des Répertoires Home des Utilisateurs**
```bash
# Vérifiez que les répertoires des utilisateurs sont correctement configurés
ls -l /home
```

#### **6. Tableau de Tests de Permission et Vérification**
Voici un tableau qui décrit les actions que chaque utilisateur essaiera de réaliser et les résultats attendus basés sur les permissions définies :

| **Action/Test**                                            | **Utilisateur** | **Commande**                                           | **Résultat Attendu**                      |
|------------------------------------------------------------|-----------------|--------------------------------------------------------|-------------------------------------------|
| Lire `file1.txt`                                           | Albert          | `cat /home/shared_data/file1.txt`                      | Succès                                    |
| Écrire dans `file1.txt`                                    | Albert          | `echo "Test" >> /home/shared_data/file1.txt`           | Succès                                    |
| Lire `file2.txt`                                           | Albert          | `cat /home/shared_data/file2.txt`                      | Succès                                    |
| Écrire dans `file2.txt`                                    | Albert          | `echo "Test" >> /home/shared_data/file2.txt`           | Échec (Permission refusée)                |
| Lire et écrire dans `file2.txt`                            | Bernard         | `echo "Bernard" >> /home/shared_data/file2.txt`        | Succès                                    |
| Exécuter `script1.sh` dans `dossier1`                      | Bernard         | `bash /home/shared_data/dossier1/script1.sh`           | Succès                                    |
| Lire et écrire dans `dossier1`                             | Claude          | `echo "Claude" >> /home/shared_data/dossier1/test.txt` | Succès                                    |
| Exécuter `script1.sh` dans `dossier1`                      | Claude          | `bash /home/shared_data/dossier1/script1.sh`           | Échec (Permission refusée)                |
| Exécuter toutes les actions sur tous les fichiers/dossiers | Danielle        | `echo "Danielle" >> /home/shared_data/file1.txt`       | Succès (accès total)                      |

#### **7. Réalisation des Tests**
```bash
# Exécuter les tests pour vérifier les permissions
su albert -c 'cat /home/shared_data/file1.txt'
su albert -c 'echo "Test" >> /home/shared_data/file2.txt'
su bernard -c 'echo "Bernard" >> /home/shared_data/file2.txt'
su bernard -c 'bash /home/shared_data/dossier1/script1.sh'
su claude -c 'echo "Claude" >> /home/shared_data/dossier1/test.txt'
su claude -c 'bash /home/shared_data/dossier1/script1.sh'
su danielle -c 'echo "Danielle" >> /home/shared_data/file1.txt'
```

### **Questions de Réflexion **

### **Objectif**: 
- Mieux comprendre la gestion des permissions dans Linux et l'impact de ces configurations sur la sécurité globale du système.


1. **Expliquez l'importance des permissions dans un système Linux. Comment les permissions incorrectes peuvent-elles affecter la sécurité d'un système ?**
   - Cette question vise à vous amener à réfléchir sur les implications de la sécurité et la gestion des accès dans un environnement Linux.

2. **Quelles différences y a-t-il entre les permissions de lecture, écriture et exécution ? Pourquoi est-il crucial de configurer correctement ces permissions dans un environnement multi-utilisateur ?**
   - Cette question est conçue pour vous aider à comprendre et à expliquer l'importance de chaque type de permission dans la sécurité et la fonctionnalité d'un système.

3. **Quel est le rôle du fichier sudoers dans la gestion des permissions système ? Comment une mauvaise configuration de ce fichier peut-elle compromettre un système Linux ?**
   - Cette question vous encourage à explorer le rôle critique du fichier sudoers dans la gestion des privilèges d'administration et les risques associés à sa mauvaise gestion.

4. **Pourquoi est-il important de limiter les permissions d'exécution sur certains fichiers ou scripts ? Donnez un exemple où cette limitation pourrait prévenir une faille de sécurité.**
   - Cette question vous permet de discuter de l'importance de la restriction des permissions d'exécution et de réfléchir à des scénarios où de telles restrictions sont essentielles à la sécurité.

5. **Comment les commandes `chmod` et `chown` influencent-elles la sécurité des fichiers et dossiers sur un serveur Linux ? Quelles sont les bonnes pratiques pour leur utilisation ?**
   - Cette question vous demande de décrire comment ces commandes affectent la sécurité des fichiers et des dossiers et de réfléchir aux meilleures pratiques pour leur utilisation efficace et sûre.

6. **Examinez un scénario où un utilisateur a accidentellement obtenu des permissions excessives sur des fichiers critiques. Quelles pourraient être les conséquences et comment ce problème pourrait-il être résolu ?**
   - Cette question vise à vous faire réfléchir aux impacts potentiels de la surattribution de permissions et aux mesures correctives possibles.

7. **Qu'est-ce que le "sticky bit" et comment peut-il être utilisé pour améliorer la sécurité des répertoires partagés ?**
   - Cette question vous encourage à explorer le concept du sticky bit, son utilité et son application dans la sécurisation des environnements où plusieurs utilisateurs accèdent aux mêmes répertoires.

8. **Discutez de l'importance de la séparation des droits d'utilisateur et d'administrateur sur un système Linux. Comment cela influence-t-il la sécurité générale du système ?**
   - Cette question vous permet de réfléchir à l'importance de la séparation des privilèges dans la prévention des abus de droits et des erreurs accidentelles.

