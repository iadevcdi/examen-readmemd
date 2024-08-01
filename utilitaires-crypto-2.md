## Rappel du cours -  Démonstrations Cryptographiques

### Démo 1 – Chiffrement de César

Le chiffrement de César est une méthode de cryptographie symétrique simple où chaque lettre du texte est décalée d'un certain nombre de positions dans l'alphabet. Par exemple, avec un décalage de 3, 'A' devient 'D', 'B' devient 'E', et ainsi de suite. La force de ce chiffrement réside dans la simplicité de sa mise en œuvre, mais il est vulnérable aux attaques par force brute ou analyse de fréquence.

### Démo 2 – DES (Data Encryption Standard)

DES est un algorithme de chiffrement par bloc qui utilise une clé de 56 bits pour chiffrer les données en blocs de 64 bits. Bien qu'ancien et considéré comme vulnérable à cause de la petite taille de sa clé (permettant des attaques par force brute), il a été largement utilisé et reste instructif pour comprendre les concepts de base du chiffrement symétrique et des modes d'opération des blocs.

### Démo 3 – AES (Advanced Encryption Standard)

AES est le successeur de DES, utilisant des clés de 128, 192 ou 256 bits pour chiffrer les données en blocs de 128 bits. Cet algorithme est actuellement l'un des standards de chiffrement les plus sûrs et les plus utilisés, employé tant dans les applications gouvernementales que commerciales. Il est résistant à toutes les attaques connues, à l'exception de celles par force brute contre les clés les plus courtes.

### Démo 4 – Génération de Hash

Le hachage est utilisé pour créer une empreinte digitale unique d'un ensemble de données. MD5 et SHA512 sont des fonctions de hachage cryptographiques. MD5 produit un hachage de 128 bits, mais il est considéré comme vulnérable à certaines attaques et donc moins sécurisé. SHA512 est une fonction de hachage plus robuste produisant un hachage de 512 bits, offrant une sécurité accrue pour les applications modernes.

### Démo 5 – Identification de Hash

Identifier le type d'algorithme de hachage utilisé pour un hash donné est crucial dans les tests de sécurité pour comprendre les vulnérabilités potentielles. Des outils comme hash-identifier aident à reconnaître le type de hash basé sur des caractéristiques et des longueurs spécifiques.

### Démo 6 – Signature numérique d'un fichier

La signature numérique permet de vérifier l'authenticité et l'intégrité d'un document. Elle utilise des clés publiques et privées pour permettre à l'émetteur de signer numériquement un document et au destinataire de vérifier la signature. Ce processus est essentiel pour des communications sécurisées et la validation de l'identité des parties dans les transactions numériques.

### Démo 7 – Attaque par texte en clair connu

Cette démonstration illustre une méthode d'attaque où l'attaquant possède à la fois un échantillon de texte en clair et son équivalent chiffré. L'objectif est d'exploiter cette information pour dériver la clé cryptographique utilisée ou pour obtenir plus d'informations sur l'algorithme de chiffrement. Cela démontre la nécessité de sécuriser non seulement les clés mais aussi les schémas de chiffrement contre de telles vulnérabilités.

Chaque démonstration couvre un aspect différent de la cryptographie, vous offrant une vue d'ensemble des méthodes, de leur application, et de leur sécurité. Ces exemples pratiques renforcent la compréhension des principes fondamentaux de la cryptographie tout en exposant les élèves à des techniques de cryptanalyse et de sécurisation des données.

## Exercices pour l'examen

### Préparation de l'environnement

1. **Mettez à jour votre gestionnaire de paquets :**
   ```bash
   sudo apt update
   ```

2. **Installez Python et pip :**
   ```bash
   sudo apt install python3 python3-pip
   ```

3. **Installez virtualenv pour créer des environnements virtuels isolés :**
   ```bash
   sudo pip3 install virtualenv
   ```

4. **Créez un environnement virtuel nommé 'hacker_ethique' dans votre répertoire de projet :**
   ```bash
   virtualenv hacker_ethique
   ```

5. **Activez l'environnement virtuel :**
   ```bash
   source hacker_ethique/bin/activate
   ```

### Démo 1 – Chiffrement de César

1. **Téléchargement du fichier caesar_cipher.py**

   Assurez-vous d'avoir téléchargé le fichier `caesar_cipher.py` depuis votre dossier GitHub.

2. **Exécution du fichier caesar_cipher.py**

   - Ouvrez votre terminal.
   - Naviguez jusqu'au répertoire où se trouve `caesar_cipher.py`.
   - Exécutez la commande suivante :
     ```bash
     python caesar_cipher.py
     ```
   - Suivez les instructions affichées pour chiffrer ou déchiffrer un texte.

### Démo 2 – DES (Data Encryption Standard)

1. **Téléchargement du fichier des.py**

   Assurez-vous d'avoir téléchargé le fichier `des.py` depuis votre dossier GitHub.

2. **Exécution du fichier des.py**

   - Ouvrez votre terminal.
   - Naviguez jusqu'au répertoire où se trouve `des.py`.
   - Exécutez la commande suivante :
     ```bash
     python des.py
     ```
   - Suivez les instructions affichées pour chiffrer ou déchiffrer un texte.

### Démo 3 – AES (Advanced Encryption Standard)

1. **Téléchargement du fichier aes_d.py**

   Assurez-vous d'avoir téléchargé le fichier `aes_d.py` depuis votre dossier GitHub.

2. **Exécution du fichier aes_d.py**

   - Ouvrez votre terminal.
   - Naviguez jusqu'au répertoire où se trouve `aes_d.py`.
   - Exécutez les commandes suivantes :
     ```bash
     pip uninstall pycrypto
     pip uninstall pycryptodome
     pip install pycryptodome
     pip list | grep pycryptodome
     python3 aes_d.py
     ```
   - Suivez les instructions affichées pour chiffrer ou déchiffrer un texte.

### Démo 4 – Génération de Hash

1. **Problème 1: Générer le hash MD5 d'un fichier texte**
   
   - **Syntaxe :**
     ```bash
     md5sum <nom_fichier> > <nom_fichier_hash>
     ```
   - **Exemple de commande :**
     ```bash
     md5sum a.txt > md5.hash
     ```

2. **Problème 2: Générer le hash SHA512 d'un fichier texte**
   
   - **Syntaxe :**
     ```bash
     sha512sum <nom_fichier> > <nom_fichier_hash>
     ```
   - **Exemple de commande :**
     ```bash
     sha512sum a.txt > sha.hash
     ```

### Démo 5 – Identification de Hash

1. **Identification de l'algorithme de hachage à partir d'un hash donné**

   - Ouvrez votre terminal.
   - Exécutez la commande suivante :
     ```bash
     hash-identifier
     ```
   - Entrez le hash et appuyez sur Entrée.
   - L'outil affichera la liste des types de hash les plus probables.

### Démo 6 – Signature numérique d'un fichier

1. **Génération des clés pour la signature numérique**

   - Ouvrez votre terminal.
   - Exécutez la commande suivante pour générer une clé :
     ```bash
     gpg --full-generate-key
     ```
   - Suivez les instructions pour sélectionner l'algorithme, entrer la taille de la clé, la validité, les détails requis et le mot de passe.
   - Les clés seront générées.

2. **Signer un fichier avec la signature numérique**
   
   - **Syntaxe :**
     ```bash
     gpg --sign <nom_fichier>
     ```
   - **Exemple de commande :**
     ```bash
     gpg --sign a.txt
     ```
   - Entrez votre mot de passe lorsque cela est demandé. Un fichier avec l'extension .gpg sera généré.

### Démo 7 – Attaque par texte en clair connu

1. **Téléchargement du fichier known_plaintext_attack.py**

   Assurez-vous d'avoir téléchargé le fichier `known_plaintext_attack.py` depuis votre dossier GitHub.

2. **Exécution du fichier known_plaintext_attack.py**

   - Ouvrez votre terminal.
   - Naviguez jusqu'au répertoire où se trouve `known_plaintext_attack.py`.
   - Exécutez la commande suivante :
     ```bash
     python known_plaintext_attack.py
     ```
   - Suivez les instructions affichées pour réaliser l'attaque par texte en clair connu.

### Codes des Fichiers

#### caesar_cipher.py

```python
string = input("Enter string: ")
shift = input("Enter shift number (Prefix 'L' for left shift and 'R' for right shift): ")

cipher = ''
if (shift[0].lower() == 'r'):
    for char in string:
        if char == ' ':
            cipher = cipher + char
        elif char.isupper():
            cipher = cipher + chr((ord(char) + int(shift[1:]) - 65) % 26 + 65)
        else:


            cipher = cipher + chr((ord(char) + int(shift[1:]) - 97) % 26 + 97)
        print(char + '->' + cipher[-1])

elif (shift[0].lower() == 'l'):
    for char in string:
        if char == ' ':
            cipher = cipher + char
        elif char.isupper():
            cipher = cipher + chr((ord(char) - int(shift[1:]) - 65) % 26 + 65)
        else:
            cipher = cipher + chr((ord(char) - int(shift[1:]) - 97) % 26 + 97)
        print(char + '->' + cipher[-1])
else:
    print("Invalid shift")

print('*************')
print('Original text: ' + string)
print('Encrypted text: ' + cipher)
```

#### des.py

```python
# Permutation tables and Sboxes
IP = (
    58, 50, 42, 34, 26, 18, 10, 2,
    60, 52, 44, 36, 28, 20, 12, 4,
    62, 54, 46, 38, 30, 22, 14, 6,
    64, 56, 48, 40, 32, 24, 16, 8,
    57, 49, 41, 33, 25, 17, 9, 1,
    59, 51, 43, 35, 27, 19, 11, 3,
    61, 53, 45, 37, 29, 21, 13, 5,
    63, 55, 47, 39, 31, 23, 15, 7
)
IP_INV = (
    40, 8, 48, 16, 56, 24, 64, 32,
    39, 7, 47, 15, 55, 23, 63, 31,
    38, 6, 46, 14, 54, 22, 62, 30,
    37, 5, 45, 13, 53, 21, 61, 29,
    36, 4, 44, 12, 52, 20, 60, 28,
    35, 3, 43, 11, 51, 19, 59, 27,
    34, 2, 42, 10, 50, 18, 58, 26,
    33, 1, 41, 9, 49, 17, 57, 25
)
PC1 = (
    57, 49, 41, 33, 25, 17, 9,
    1, 58, 50, 42, 34, 26, 18,
    10, 2, 59, 51, 43, 35, 27,
    19, 11, 3, 60, 52, 44, 36,
    63, 55, 47, 39, 31, 23, 15,
    7, 62, 54, 46, 38, 30, 22,
    14, 6, 61, 53, 45, 37, 29,
    21, 13, 5, 28, 20, 12, 4
)
PC2 = (
    14, 17, 11, 24, 1, 5,
    3, 28, 15, 6, 21, 10,
    23, 19, 12, 4, 26, 8,
    16, 7, 27, 20, 13, 2,
    41, 52, 31, 37, 47, 55,
    30, 40, 51, 45, 33, 48,
    44, 49, 39, 56, 34, 53,
    46, 42, 50, 36, 29, 32
)

E = (
    32, 1, 2, 3, 4, 5,
    4, 5, 6, 7, 8, 9,
    8, 9, 10, 11, 12, 13,
    12, 13, 14, 15, 16, 17,
    16, 17, 18, 19, 20, 21,
    20, 21, 22, 23, 24, 25,
    24, 25, 26, 27, 28, 29,
    28, 29, 30, 31, 32, 1
)

Sboxes = {
    0: (
        14, 4, 13, 1, 2, 15, 11, 8, 3, 10, 6, 12, 5, 9, 0, 7,
        0, 15, 7, 4, 14, 2, 13, 1, 10, 6, 12, 11, 9, 5, 3, 8,
        4, 1, 14, 8, 13, 6, 2, 11, 15, 12, 9, 7, 3, 10, 5, 0,
        15, 12, 8, 2, 4, 9, 1, 7, 5, 11, 3, 14, 10, 0, 6, 13
    ),
    1: (
        15, 1, 8, 14, 6, 11, 3, 4, 9, 7, 2, 13, 12, 0, 5, 10,
        3, 13, 4, 7, 15, 2, 8, 14, 12, 0, 1, 10, 6, 9, 11, 5,
        0, 14, 7, 11, 10, 4, 13, 1, 5, 8, 12, 6, 9, 3, 2, 15,
        13, 8, 10, 1, 3, 15, 4, 2, 11, 6, 7, 12, 0, 5, 14, 9
    ),
    2: (
        10, 0, 9, 14, 6, 3, 15, 5, 1, 13, 12, 7, 11, 4, 2, 8,
        13, 7, 0, 9, 3, 4, 6, 10, 2, 8, 5, 14, 12, 11, 15, 1,
        13, 6, 4, 9, 8, 15, 3, 0, 11, 1, 2, 12, 5, 10, 14, 7,
        1, 10, 13, 0, 6, 9, 8, 7, 4, 15, 14, 3, 11, 5, 2, 12
    ),
    3: (
        7, 13, 14, 3, 0, 6, 9, 10, 1, 2, 8, 5, 11, 12, 4, 15,
        13, 8, 11, 5, 6, 15, 0, 3, 4, 7, 2, 12, 1, 10, 14, 9,
        10, 6, 9, 0, 12, 11, 7, 13, 15, 1, 3, 14, 5, 2, 8, 4,
        3, 15, 0, 6, 10, 1, 13, 8, 9, 4, 5, 11, 12, 7, 2, 14
    ),
    4: (
        2, 12, 4, 1, 7, 10, 11, 6, 8, 5, 3, 15, 13, 0, 14, 9,
        14, 11, 2, 12, 4, 7, 13, 1, 5, 0, 15, 10, 3, 9, 8, 6,
        4, 2, 1, 11, 10, 13, 7, 8, 

15, 9, 12, 5, 6, 3, 0, 14,
        11, 8, 12, 7, 1, 14, 2, 13, 6, 15, 0, 9, 10, 4, 5, 3
    ),
    5: (
        12, 1, 10, 15, 9, 2, 6, 8, 0, 13, 3, 4, 14, 7, 5, 11,
        10, 15, 4, 2, 7, 12, 9, 5, 6, 1, 13, 14, 0, 11, 3, 8,
        9, 14, 15, 5, 2, 8, 12, 3, 7, 0, 4, 10, 1, 13, 11, 6,
        4, 3, 2, 12, 9, 5, 15, 10, 11, 14, 1, 7, 6, 0, 8, 13
    ),
    6: (
        4, 11, 2, 14, 15, 0, 8, 13, 3, 12, 9, 7, 5, 10, 6, 1,
        13, 0, 11, 7, 4, 9, 1, 10, 14, 3, 5, 12, 2, 15, 8, 6,
        1, 4, 11, 13, 12, 3, 7, 14, 10, 15, 6, 8, 0, 5, 9, 2,
        6, 11, 13, 8, 1, 4, 10, 7, 9, 5, 0, 15, 14, 2, 3, 12
    ),
    7: (
        13, 2, 8, 4, 6, 15, 11, 1, 10, 9, 3, 14, 5, 0, 12, 7,
        1, 15, 13, 8, 10, 3, 7, 4, 12, 5, 6, 11, 0, 14, 9, 2,
        7, 11, 4, 1, 9, 12, 14, 2, 0, 6, 10, 13, 15, 3, 5, 8,
        2, 1, 14, 7, 4, 10, 8, 13, 15, 12, 9, 0, 3, 5, 6, 11
    )
}

P = (
    16, 7, 20, 21,
    29, 12, 28, 17,
    1, 15, 23, 26,
    5, 18, 31, 10,
    2, 8, 24, 14,
    32, 27, 3, 9,
    19, 13, 30, 6,
    22, 11, 4, 25
)


def encrypt(msg, key, decrypt=False):
    # only encrypt single blocks
    assert isinstance(msg, int) and isinstance(key, int)
    assert not msg.bit_length() > 64
    assert not key.bit_length() > 64

    # permutate by table PC1
    key = permutation_by_table(key, 64, PC1)  # 64bit -> PC1 -> 56bit

    # split up key in two halves
    # generate the 16 round keys
    C0 = key >> 28
    D0 = key & (2 ** 28 - 1)
    round_keys = generate_round_keys(C0, D0)  # 56bit -> PC2 -> 48bit

    msg_block = permutation_by_table(msg, 64, IP)
    L0 = msg_block >> 32
    R0 = msg_block & (2 ** 32 - 1)

    # apply thr round function 16 times in following scheme (feistel cipher):
    L_last = L0
    R_last = R0
    for i in range(1, 17):
        if decrypt:  # just use the round keys in reversed order
            i = 17 - i
        L_round = R_last
        R_round = L_last ^ round_function(R_last, round_keys[i])
        L_last = L_round
        R_last = R_round
        print("---- Round "+str(i)+"----")
        print("L0= %s, R0= %s, L1=%s, R1+%s" %(L_last, R_last, L_round, R_round))

    # concatenate reversed
    cipher_block = (R_round << 32) + L_round

    # final permutation
    cipher_block = permutation_by_table(cipher_block, 64, IP_INV)

    return cipher_block


def round_function(Ri, Ki):
    # expand Ri from 32 to 48 bit using table E
    Ri = permutation_by_table(Ri, 32, E)

    # xor with round key
    Ri ^= Ki

    # split Ri into 8 groups of 6 bit
    Ri_blocks = [((Ri & (0b111111 << shift_val)) >> shift_val) for shift_val in (42, 36, 30, 24, 18, 12, 6, 0)]

    # interpret each block as address for the S-boxes
    for i, block in enumerate(Ri_blocks):
        # grab the bits we need
        row = ((0b100000 & block) >> 4) + (0b1 & block)
        col = (0b011110 & block) >> 1
        # sboxes are stored as one-dimensional tuple, so we need to calc the index this way
        Ri_blocks[i] = Sboxes[i][16 * row + col]

    # pack the blocks together again by concatenating
    Ri_blocks = zip(Ri_blocks, (28, 24, 20, 16, 12, 8, 4, 0))
    Ri = 0
    for block, lshift_val in Ri_blocks:
        Ri += (block << lshift_val)

    # another permutation 32bit -> 32bit
    Ri = permutation_by_table(Ri, 32, P)

    return Ri


def permutation_by_table(block, block_len, table):
    # quick and dirty casting to str
    block_str = bin(block)[2:].zfill(block_len)
    perm = []
    for pos in range(len(table)):
        perm.append(block_str[table[pos] - 1])
    return int(''.join(perm), 2)


def generate_round_keys(C0, D0):
    # returns dict of 16 keys (one for each round)

    round_keys = dict.fromkeys(range(0, 17))
    lrot_values = (1, 1, 2, 2, 2, 2, 2, 2, 1, 2, 2, 2, 2, 2, 2, 1)

    # left-rotation function
    lrot = lambda val, r_bits, max_bits: \
        (val << r_bits % max_bits) & (2 ** max_bits - 1) | \
        ((val & (2 ** max_bits - 1)) >> (max_bits - (r_bits % max_bits)))

    # initial rotation
    C0 = lrot(C0, 0, 28)
    D0 = lrot(D0, 0, 28)
    round_keys[0] = (C0, D0)

    # create 16 more different key pairs
    for i, rot_val in enumerate(lrot_values):
        i += 1
        Ci = lrot(round_keys[i - 1][0], rot_val, 28)
        Di = lrot(round_keys[i - 1][1], rot_val, 28)
        round_keys[i] = (Ci, Di)

    # round_keys[1] for first round
    #           [16] for 16th round
    # dont need round_keys[0] anymore, remove
    del round_keys[0]

    # now form the keys from concatenated CiDi 1<=i<=16 and by apllying PC2
    for i, (Ci, Di) in round_keys.items():
        Ki = (Ci << 28) + Di
        round_keys[i] = permutation_by_table(Ki, 56, PC2)  # 56bit -> 48bit

    return round_keys


k = 0x0e329232ea6d0d73  # 64 bit
k2 = 0x133457799BBCDFF1
m = 0x8787878787878787
m2 = 0x0123456789ABCDEF




def prove(key, msg):
    print('key:       {:x}'.format(key))
    print('message:   {:x}'.format(msg))
    cipher_text = encrypt(msg, key)
    print('encrypted: {:x}'.format(cipher_text))
    plain_text = encrypt(cipher_text, key, decrypt=True)
    print('decrypted: {:x}'.format(plain_text))
```

#### known_plaintext_attack.py

```python
cipher = input("Enter the text encrypted using Caeser's cipher: ")
original = input("Enter the plain text of the first world/letter: ")

og_len = len(original)
sub_cipher = cipher[:og_len]

for i in range(0, 28):
    temp = ''
    string = original[0:og_len]
    for char in string:
        if char == ' ':
            temp = temp + char
        elif char.isupper():
            temp = temp + chr((ord(char) + i - 65) % 26 + 65)
        else:
            temp = temp+ chr((ord(char) + i - 97) % 26 + 97)
    if (temp == sub_cipher):
        print ("Shift towards right.\nKey= "+str(i))
        break

for i in range(0, 28):
    temp = ''
    string = original[0:og_len]
    for char in string:
        if char == ' ':
            temp = temp + char
        elif char.isupper():
            temp = temp + chr((ord(char) - i - 65) % 26 + 65)
        else:
            temp = temp + chr((ord(char) - i - 97) % 26 + 97)
    if (temp == sub_cipher):
        print("Shift towards left.\nKey= " + str(i))
        break
```

# Annexe QUESTIONS/RÉPONSES: 

Voici des réponses exhaustives aux questions de réflexion pour chaque démonstration de cryptographie. Ces réponses peuvent être ajoutées aux annexes de votre cours.

## Réponses aux Questions de Réflexion

### Démo 1 – Chiffrement de César

1. **Pourquoi le chiffrement de César est-il vulnérable aux attaques par force brute ?**

   Le chiffrement de César utilise un décalage fixe pour chaque lettre de l'alphabet, ce qui signifie qu'il n'y a que 25 décalages possibles (1 à 25, car un décalage de 0 ne change pas le texte). Cela rend l'algorithme très vulnérable aux attaques par force brute, où un attaquant peut simplement essayer chaque décalage jusqu'à trouver le bon. La simplicité de l'algorithme, qui est un de ses avantages, devient ici une faiblesse, car elle permet à un attaquant de tester rapidement toutes les clés possibles.

2. **Comment une analyse de fréquence pourrait-elle être utilisée pour briser un chiffrement de César ?**

   Dans une langue naturelle, certaines lettres apparaissent plus fréquemment que d'autres. Par exemple, en anglais, les lettres 'E', 'T', 'A', 'O', 'I', 'N', 'S', 'H', 'R' apparaissent souvent. Si un texte chiffré utilise un chiffrement de César, la fréquence des lettres chiffrées peut être comparée aux fréquences attendues des lettres en clair. En identifiant les lettres chiffrées les plus fréquentes et en les mappant aux lettres en clair les plus fréquentes, un attaquant peut déduire le décalage utilisé et ainsi déchiffrer le message.

3. **Quels sont les avantages et les inconvénients de la simplicité du chiffrement de César ?**

   **Avantages :**
   - Facile à comprendre et à implémenter.
   - Ne nécessite pas de technologie avancée, ce qui le rend utilisable à la main.

   **Inconvénients :**
   - Très faible en termes de sécurité, vulnérable aux attaques par force brute et par analyse de fréquence.
   - Non sécurisé pour des communications sensibles ou confidentielles.
   - Peut être facilement déchiffré par des méthodes simples d'analyse manuelle ou avec des outils automatisés.

### Démo 2 – DES (Data Encryption Standard)

1. **Pourquoi la petite taille de la clé de DES le rend-elle vulnérable aux attaques par force brute ?**

   La clé de DES est de 56 bits, ce qui signifie qu'il y a \(2^{56}\) combinaisons possibles. Bien que cela puisse sembler beaucoup, les capacités des ordinateurs modernes permettent de tester ces combinaisons en un temps relativement court. Des attaques par force brute sur DES ont été réalisées avec succès, notamment par des organisations utilisant des réseaux de calcul distribué ou des ordinateurs spécialement conçus pour cette tâche. En comparaison, les standards modernes comme AES utilisent des clés de 128, 192 ou 256 bits, rendant les attaques par force brute impraticables avec la technologie actuelle.

2. **Quels concepts fondamentaux du chiffrement symétrique et des modes d'opération des blocs sont illustrés par DES ?**

   DES illustre plusieurs concepts clés de la cryptographie symétrique :
   - **Permutation et Substitution** : DES utilise des permutations (réarrangement des bits) et des substitutions (remplacement des bits par d'autres selon des règles définies) pour sécuriser les données.
   - **Clé de chiffrement** : Une clé secrète partagée est utilisée pour chiffrer et déchiffrer les données.
   - **Feistel Network** : DES utilise une structure de Feistel, où le texte clair est divisé en deux moitiés, et chaque moitié est manipulée et combinée dans plusieurs tours pour produire le texte chiffré.
   - **Modes d'opération** : Bien que DES soit un chiffrement par bloc, il est souvent utilisé avec des modes d'opération comme CBC (Cipher Block Chaining) pour chiffrer des données plus grandes qu'un seul bloc de 64 bits.

3. **Pourquoi DES, bien qu'obsolète, reste-t-il important pour l'apprentissage de la cryptographie ?**

   DES est un algorithme fondamental dans l'histoire de la cryptographie moderne. Il a été l'un des premiers algorithmes de chiffrement largement adoptés et standardisés, et a influencé de nombreux autres algorithmes. Apprendre DES permet de comprendre les bases du chiffrement symétrique, les structures de Feistel, et les concepts de permutation et substitution. De plus, l'étude des faiblesses de DES, telles que les attaques par force brute et les attaques différentielles, aide à comprendre pourquoi des algorithmes plus modernes comme AES ont été développés.

### Démo 3 – AES (Advanced Encryption Standard)

1. **En quoi AES diffère-t-il de DES en termes de sécurité et de performance ?**

   **Sécurité :**
   - AES utilise des clés de longueur 128, 192 ou 256 bits, comparé aux 56 bits de DES, ce qui rend AES beaucoup plus résistant aux attaques par force brute.
   - AES a été conçu pour résister à un large éventail d'attaques, y compris les attaques linéaires et différentielles.

   **Performance :**
   - AES est plus rapide et plus efficace sur les matériels modernes, en particulier ceux qui supportent les instructions AES-NI (Advanced Encryption Standard New Instructions).
   - AES fonctionne sur des blocs de 128 bits, ce qui est plus adapté aux architectures modernes et aux volumes de données plus importants.

2. **Pourquoi AES est-il considéré comme l'un des standards de chiffrement les plus sûrs actuellement ?**

   AES est considéré comme sûr en raison de sa résistance aux attaques connues et de la longueur de ses clés. Même avec des clés de 128 bits, AES offre une sécurité qui dépasse de loin les capacités de calcul actuelles pour les attaques par force brute. Les versions avec des clés de 192 et 256 bits offrent une sécurité supplémentaire pour des applications critiques. De plus, AES a été soigneusement analysé par la communauté cryptographique mondiale et est largement utilisé dans les applications gouvernementales, militaires et commerciales.

3. **Quels sont les défis liés à la mise en œuvre d'AES par rapport à DES ?**

   La mise en œuvre d'AES peut être plus complexe en raison de ses transformations mathématiques (substitution, permutation, et multiplication dans un champ de Galois), mais cette complexité est gérable avec les ressources et les outils modernes. La principale difficulté réside dans la gestion sécurisée des clés et la mise en œuvre correcte des modes d'opération pour s'assurer que les données restent protégées même dans des scénarios de chiffrement de volume de données important.

### Démo 4 – Génération de Hash

1. **Pourquoi MD5 est-il considéré comme vulnérable et moins sécurisé ?**

   MD5 est considéré comme vulnérable car il produit des collisions, c'est-à-dire des situations où deux entrées différentes génèrent le même hachage. Cela permet à un attaquant de substituer un fichier ou un message par un autre tout en conservant le même hachage, compromettant ainsi l'intégrité des données. Des attaques pratiques ont montré que des collisions peuvent être trouvées en un temps raisonnable, ce qui rend MD5 inapproprié pour les applications nécessitant une sécurité forte.

2. **Quels sont les avantages de SHA512 par rapport à MD5 ?**

   SHA512 offre une sécurité bien supérieure à MD5 en raison de sa taille de hachage plus longue (512 bits contre 128 bits pour MD5) et de sa résistance accrue aux collisions. SHA512 est également conçu pour être plus robuste contre les attaques de force brute et les attaques de préimage. En conséquence, SHA512 est recommandé pour les applications nécessitant une intégrité et une sécurité renforcées, comme les signatures numériques et la vérification des intégrités des fichiers.

3. **Dans quels scénarios l'utilisation de fonctions de hachage est-elle essentielle ?**

   Les fonctions de hachage sont essentielles dans de nombreux scénarios, notamment :
   - **Signatures numériques** : Pour garantir l'intégrité et l'authenticité des messages.
   - **Intégrité des fichiers** : Pour vérifier que les fichiers n'ont pas été modifiés.
   - **Stockage des mots de passe** : Les mots de passe sont souvent hachés avant d'être stockés pour éviter qu'ils soient lisibles en cas de compromission de la base de données.
   - **Génération d'identifiants uniques** : Pour créer des identifiants uniques pour les données sans révéler les informations sensibles sous-jacentes.

### Démo 5 – Identification de Hash

1. **Pourquoi est-il important de pouvoir identifier le type d'algorithme de hachage utilisé ?**

   Identifier le type d'algorithme de hachage est crucial pour analyser les vulnérabilités potentielles et comprendre les risques de sécurité associés. Connaître l'algorithme permet de déterminer la robustesse du hachage et de savoir si des attaques connues peuvent être appliquées. Cela aide également à choisir des méthodes de protection appropriées et à mettre en œuvre des contre-mesures efficaces.

2. **Comment l'outil hash-identifier aide-t-il dans les tests de sécurité ?**

   L'outil hash-identifier aide les testeurs de sécurité à reconnaître rapidement et avec précision le type de hash utilisé en fonction de la longueur et des caractéristiques du hash. Cela permet d'évaluer rapidement la sécurité du hachage et

 de déterminer si des mesures supplémentaires doivent être prises pour protéger les données. L'outil peut également être utilisé pour valider que les fonctions de hachage appropriées sont utilisées dans les applications.

3. **Quels pourraient être les défis ou les limitations de l'utilisation de hash-identifier ?**

   Les défis et limitations de l'utilisation de hash-identifier incluent :
   - **Exactitude** : Bien que hash-identifier soit précis pour de nombreux hachages courants, il peut ne pas reconnaître des algorithmes de hachage moins connus ou propriétaires.
   - **Longueur des Hashes** : Certains algorithmes de hachage produisent des résultats de longueur variable, ce qui peut compliquer l'identification.
   - **Mises à jour** : Les algorithmes de hachage évoluent, et l'outil doit être régulièrement mis à jour pour inclure de nouveaux types de hachages et leurs caractéristiques.

### Démo 6 – Signature numérique d'un fichier

1. **Comment les signatures numériques assurent-elles l'authenticité et l'intégrité d'un document ?**

   Les signatures numériques utilisent des clés cryptographiques publiques et privées pour signer et vérifier des documents. Lorsque l'émetteur signe un document avec sa clé privée, il génère une signature unique basée sur le contenu du document. Le destinataire peut alors utiliser la clé publique de l'émetteur pour vérifier que la signature correspond au document et que celui-ci n'a pas été altéré. Cela assure l'authenticité (le document provient bien de l'émetteur) et l'intégrité (le document n'a pas été modifié depuis sa signature).

2. **Pourquoi la génération et la gestion des clés sont-elles cruciales dans le processus de signature numérique ?**

   La sécurité des signatures numériques repose sur la protection des clés privées et la distribution correcte des clés publiques. Si une clé privée est compromise, un attaquant peut générer des signatures valides pour des documents falsifiés. De même, si une clé publique n'est pas distribuée de manière sécurisée, un attaquant pourrait substituer une fausse clé publique, compromettant la vérification des signatures. La gestion des clés, y compris leur génération, stockage et révocation, est donc essentielle pour maintenir la sécurité du système de signature numérique.

3. **Quels sont les avantages de l'utilisation des signatures numériques dans les transactions numériques ?**

   Les signatures numériques offrent plusieurs avantages dans les transactions numériques :
   - **Sécurité** : Elles assurent l'intégrité et l'authenticité des documents.
   - **Non-répudiation** : Une signature numérique valide prouve que le signataire ne peut nier avoir signé le document.
   - **Efficacité** : Elles permettent des vérifications rapides et automatisées de l'intégrité et de l'authenticité.
   - **Fiabilité** : Elles sont largement reconnues et utilisées dans des applications variées, des contrats électroniques aux transactions financières.

### Démo 7 – Attaque par texte en clair connu

1. **Pourquoi les attaques par texte en clair connu sont-elles possibles et comment peuvent-elles être prévenues ?**

   Les attaques par texte en clair connu sont possibles lorsque l'attaquant a accès à une partie du texte clair ainsi que son équivalent chiffré. Cela lui permet de déduire des informations sur le schéma de chiffrement ou la clé utilisée. Pour prévenir ces attaques :
   - Utilisez des schémas de chiffrement robustes et modernes.
   - Employez des vecteurs d'initialisation (IV) pour chaque message chiffré afin d'empêcher les modèles répétitifs.
   - Assurez-vous que les clés de chiffrement sont bien protégées et régulièrement mises à jour.

2. **Quelles informations peuvent être dérivées d'une attaque par texte en clair connu ?**

   Une attaque par texte en clair connu peut permettre à l'attaquant de :
   - Déduire la clé de chiffrement utilisée, ce qui permet de déchiffrer d'autres messages chiffrés avec la même clé.
   - Obtenir des informations sur l'algorithme de chiffrement, ce qui peut mener à des vulnérabilités exploitables.
   - Découvrir des modèles ou des faiblesses dans le schéma de chiffrement utilisé.

3. **Quels sont les contre-mesures efficaces contre les attaques par texte en clair connu ?**

   Pour se protéger contre les attaques par texte en clair connu :
   - Utilisez des algorithmes de chiffrement modernes comme AES, qui sont résistants à de telles attaques.
   - Mettez en œuvre des modes d'opération sécurisés comme CBC ou GCM avec des IV uniques et aléatoires pour chaque chiffrement.
   - Protégez les clés de chiffrement en les stockant de manière sécurisée et en les changeant régulièrement.
   - Évitez de réutiliser les mêmes clés pour chiffrer des messages différents.
