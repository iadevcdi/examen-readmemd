### Exercice 1: Chiffrement et Déchiffrement avec GPG
GPG (GNU Privacy Guard) est un outil de chiffrement qui permet de sécuriser les communications et les données.

#### Objectifs:
- Créer une paire de clés GPG
- Chiffrer un fichier
- Déchiffrer un fichier

#### Étapes détaillées:

1. **Créer une paire de clés GPG**:
    - Ouvrez un terminal.
    - Tapez la commande suivante et suivez les instructions:
    ```sh
    gpg --full-generate-key
    ```
    - Choisissez `(1) RSA and RSA (default)`.
    - Indiquez une taille de clé de `2048` bits.
    - Choisissez une durée de validité de la clé (par exemple `0` pour une durée illimitée).
    - Fournissez votre nom, votre adresse e-mail et un commentaire (optionnel).
    - Entrez une phrase de passe sécurisée lorsque cela est demandé.
    - Une fois la clé générée, vous devriez voir un message de confirmation.

2. **Exporter la clé publique**:
    - La clé publique est utilisée pour chiffrer les messages que seuls le propriétaire de la clé privée peut déchiffrer.
    - Utilisez la commande suivante pour exporter votre clé publique dans un fichier:
    ```sh
    gpg --export -a "Votre Nom" > clé_publique.asc
    ```

3. **Créer un fichier texte**:
    - Créez un fichier texte avec un message secret:
    ```sh
    echo "Ceci est un message secret" > message.txt
    ```

4. **Chiffrer le fichier**:
    - Utilisez la clé publique pour chiffrer le fichier texte:
    ```sh
    gpg --output message.txt.gpg --encrypt --recipient "Votre Nom" message.txt
    ```
    - Cette commande crée un fichier chiffré nommé `message.txt.gpg`.

5. **Déchiffrer le fichier**:
    - Utilisez votre clé privée pour déchiffrer le fichier:
    ```sh
    gpg --output message_dechiffre.txt --decrypt message.txt.gpg
    ```
    - Cette commande crée un fichier texte nommé `message_dechiffre.txt` contenant le message original.

### Exercice 2: Génération et Utilisation de Clés SSL avec OpenSSL
OpenSSL est une boîte à outils puissante pour les protocoles de cryptographie.

#### Objectifs:
- Générer une clé privée
- Générer une CSR (Certificate Signing Request)
- Générer un certificat auto-signé

#### Étapes détaillées:

1. **Générer une clé privée**:
    - La clé privée est utilisée pour créer des signatures numériques et pour déchiffrer des données chiffrées avec la clé publique correspondante.
    - Utilisez la commande suivante pour générer une clé privée protégée par un mot de passe:
    ```sh
    openssl genpkey -algorithm RSA -out clé_privée.pem -aes256
    ```
    - Vous serez invité à entrer et confirmer une phrase de passe.

2. **Créer une CSR**:
    - Une CSR est utilisée pour demander un certificat numérique à une autorité de certification (CA).
    - Utilisez la commande suivante pour créer une CSR:
    ```sh
    openssl req -new -key clé_privée.pem -out demande_certificat.csr
    ```
    - Remplissez les champs demandés, tels que le nom de votre pays, votre état, votre ville, votre organisation, etc.

3. **Générer un certificat auto-signé**:
    - Pour les tests ou pour des utilisations internes, vous pouvez créer un certificat auto-signé.
    - Utilisez la commande suivante pour générer un certificat auto-signé valide pendant un an (365 jours):
    ```sh
    openssl x509 -req -days 365 -in demande_certificat.csr -signkey clé_privée.pem -out certificat_autosigné.crt
    ```

### Exercice 3: Génération de Clés SSH avec ssh-keygen
`ssh-keygen` est un outil pour créer des paires de clés SSH pour une authentification sécurisée.

#### Objectifs:
- Générer une paire de clés SSH
- Copier la clé publique sur un serveur distant
- Utiliser la clé pour se connecter au serveur

#### Étapes détaillées:

1. **Générer une paire de clés SSH**:
    - La paire de clés SSH consiste en une clé privée et une clé publique.
    - Utilisez la commande suivante pour générer une paire de clés:
    ```sh
    ssh-keygen -t rsa -b 2048 -f ~/.ssh/id_rsa
    ```
    - Vous pouvez accepter les valeurs par défaut en appuyant sur `Entrée`.
    - Entrez une phrase de passe pour protéger la clé privée (optionnel mais recommandé).

2. **Copier la clé publique sur un serveur distant**:
    - La commande suivante copie votre clé publique sur un serveur distant pour une authentification par clé publique:
    ```sh
    ssh-copy-id utilisateur@serveur_distant
    ```
    - Remplacez `utilisateur` par votre nom d'utilisateur et `serveur_distant` par l'adresse du serveur.

3. **Se connecter au serveur avec la clé SSH**:
    - Utilisez la commande suivante pour vous connecter au serveur sans mot de passe:
    ```sh
    ssh utilisateur@serveur_distant
    ```

### Exercice 4: Chiffrement et Déchiffrement de Fichiers avec OpenSSL
OpenSSL peut également être utilisé pour chiffrer et déchiffrer des fichiers.

#### Objectifs:
- Chiffrer un fichier
- Déchiffrer un fichier

#### Étapes détaillées:

1. **Créer un fichier texte**:
    - Créez un fichier texte avec un message secret:
    ```sh
    echo "Ceci est un autre message secret" > secret.txt
    ```

2. **Chiffrer le fichier**:
    - Utilisez OpenSSL pour chiffrer le fichier avec AES-256:
    ```sh
    openssl enc -aes-256-cbc -salt -in secret.txt -out secret.txt.enc
    ```
    - Vous serez invité à entrer et confirmer une phrase de passe.

3. **Déchiffrer le fichier**:
    - Utilisez OpenSSL pour déchiffrer le fichier:
    ```sh
    openssl enc -d -aes-256-cbc -in secret.txt.enc -out secret_dechiffre.txt
    ```
    - Entrez la phrase de passe que vous avez utilisée pour chiffrer le fichier.

