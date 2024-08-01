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

### **Conclusion**
Ce guide complet fournit toutes les étapes, de la configuration à la vérification, pour assurer que les permissions et les accès sont correctement attribués et fonctionnels.
