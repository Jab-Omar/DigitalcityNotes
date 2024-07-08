### Introduction

Le Contrôle de Redondance Cyclique (CRC) est une technique de détection d'erreurs utilisée dans les réseaux et les systèmes de stockage pour vérifier l'intégrité des données. Il permet de détecter les erreurs qui peuvent survenir lors de la transmission ou du stockage des données.

### Principe de Fonctionnement

Le CRC est basé sur les mathématiques des polynômes. Lorsqu'un message ou un bloc de données est envoyé, un CRC est calculé et ajouté à la fin des données. À la réception, le CRC est recalculé et comparé au CRC reçu. Si les deux CRC correspondent, les données sont considérées comme intactes ; sinon, une erreur est détectée.

### Calcul du CRC

1. **Polynôme Générateur** : Un polynôme prédéfini, appelé polynôme générateur, est utilisé pour calculer le CRC. Par exemple, CRC-32 utilise le polynôme `0x04C11DB7`.
2. **Division Binaire** : Les données à transmettre sont considérées comme un polynôme binaire et sont divisées par le polynôme générateur en utilisant une division binaire modulo 2.
3. **Reste** : Le reste de cette division est le CRC, qui est ajouté aux données initiales.

### Étapes de Calcul du CRC

1. **Ajout de Zéros** : Ajouter un nombre de zéros égal à la longueur du CRC à la fin des données.
2. **Division** : Diviser le message étendu (données + zéros) par le polynôme générateur en utilisant une division binaire.
3. **Reste** : Le reste de cette division est le CRC. Il est ajouté à la fin des données originales.

### Exemple de Calcul du CRC

1. **Données** : `11010011101100`
2. **Polynôme Générateur** : `1011`
3. **Données Étendues** : `11010011101100000` (ajout de trois zéros car le polynôme générateur a une longueur de 4 bits)
4. **Division** :
    - `1101 0011 1011 0000` (données étendues)
    - Diviser par `1011`
    - Processus de division binaire, bit par bit
5. **Reste** : Le reste de cette division binaire est le CRC, par exemple `100`.

### Utilisation du CRC dans les Réseaux

Le CRC est largement utilisé dans les protocoles réseau pour assurer l'intégrité des données transmises :

- **Ethernet** : Utilise CRC-32 pour vérifier les trames.
- **PPP (Point-to-Point Protocol)** : Utilise CRC-16 ou CRC-32 selon la variante.
- **Wi-Fi** : Utilise CRC pour les trames de niveau MAC.

### Avantages du CRC

- **Détection d'Erreurs** : Très efficace pour détecter des erreurs courantes telles que les inversions de bits et les décalages.
- **Simplicité** : Relativement simple à implémenter en matériel et en logiciel.
- **Efficacité** : Rapide à calculer et ne nécessite pas beaucoup de ressources.

### Limites du CRC

- **Correction d'Erreurs** : Le CRC ne corrige pas les erreurs, il les détecte seulement.
- **Vulnérabilité** : Des erreurs multiples peuvent parfois passer inaperçues (collision de CRC).

### Exercice Pratique

1. **Calcul du CRC en Python** :
    - Écrire un script Python pour calculer le CRC d'une chaîne binaire donnée en utilisant un polynôme générateur spécifié.

```python
def xor(a, b):
    result = []
    for i in range(1, len(b)):
        if a[i] == b[i]:
            result.append('0')
        else:
            result.append('1')
    return ''.join(result)

def mod2div(dividend, divisor):
    pick = len(divisor)
    tmp = dividend[0:pick]
    
    while pick < len(dividend):
        if tmp[0] == '1':
            tmp = xor(divisor, tmp) + dividend[pick]
        else:
            tmp = xor('0'*pick, tmp) + dividend[pick]
        pick += 1

    if tmp[0] == '1':
        tmp = xor(divisor, tmp)
    else:
        tmp = xor('0'*pick, tmp)
    
    return tmp

def encodeData(data, key):
    l_key = len(key)
    appended_data = data + '0'*(l_key-1)
    remainder = mod2div(appended_data, key)
    codeword = data + remainder
    return codeword

data = "11010011101100"
key = "1011"
print("Data:", data)
print("Polynomial Key:", key)
encoded_data = encodeData(data, key)
print("Encoded Data with CRC:", encoded_data)
```

### Conclusion

Le Contrôle de Redondance Cyclique (CRC) est un outil essentiel pour garantir l'intégrité des données dans les réseaux. Il offre une méthode efficace pour détecter les erreurs qui peuvent survenir lors de la transmission ou du stockage des données.