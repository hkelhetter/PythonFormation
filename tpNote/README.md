# Analyse achat

## 1. **Métriques**

- `price` (montant des articles)
- `freight_value` (valeur du fret)
- `name_lenght` (longueur des noms de produits)
- `description_lenght` (longueur des descriptions)
- `photos_qty` (nombre de photos)
- `weight_g` (poids en grammes)
- `length_cm` (longueur en cm)
- `height_cm` (hauteur en cm)
- `width_cm` (largeur en cm)

## 2. **Dimensions**

### A. **Commandes et produits**

- `order_id` (identifiant de commande)
- `order_item_id` (identifiant d'item dans la commande)
- `product_id` (identifiant produit)
- `category_name` (catégorie de produit)
- `status` (statut de la commande)

### B. **Clients**

- `customer_id` (identifiant client)
- `customer_unique_id` (identifiant unique client)
- `cust_zip_code` (code postal client)
- `cust_city` (ville client)
- `cust_state` (état client)
- `cust_name_state` (nom et état client)

### C. **Vendeurs**

- `seller_id` (identifiant vendeur)
- `sell_zip_code` (code postal vendeur)
- `sell_city` (ville vendeur)
- `sell_state` (état vendeur)
- `sell_name_state` (nom et état vendeur)

### D. **Temps**

- **Dates principales :**
    - `purchase_timestamp` (heure d'achat)
    - `approved_at` (date d'approbation)
    - `delivered_carrier` (date livraison transporteur)
    - `delivered_customer` (date livraison client)
    - `estimated_delivery` (date estimée de livraison)

- **Découpages temporels :**
    - `annee`, `mois`, `annee_mois`, `jour`, `annee_jour`
    - `jour_semaine`, `trimestre`, `annee_trimestre`
    - `semaine`, `annee_semaine`, `heure`

## 3. **Hiérarchies**

### A. **Temps**

1. **Hiérarchie annuelle :**
    - `annee` > `trimestre` > `mois` > `jour` > `heure`
2. **Hiérarchie hebdomadaire :**
    - `annee` > `semaine` > `jour_semaine`

### B. **Localisation**

1. **Client :**
    - `cust_state` > `cust_city` > `cust_zip_code`
2. **Vendeur :**
    - `sell_state` > `sell_city` > `sell_zip_code`

### C. **Commande**

- `order_id` > `order_item_id`

### D. **Produit**

- `category_name` > `product_id`

# Analyse Vente

## 1. Métriques

- Paiements :
    - `value_boleto` (valeur par boleto)
    - `value_credit_card` (valeur par carte de crédit)
    - `value_debit_card` (valeur par carte de débit)
    - `value_not_defined` (valeur par méthode indéfinie)
    - `value_voucher` (valeur par voucher)

- Interactions :
    - `int_boleto` (nombre d'interactions boleto)
    - `int_credit_card` (nombre d'interactions carte de crédit)
    - `int_debit_card` (nombre d'interactions carte de débit)
    - `int_not_defined` (nombre d'interactions méthode indéfinie)
    - `int_voucher` (nombre d'interactions voucher)

- Scores et évaluations :
    - `score_1`, `score_2`, `score_3`, `score_4`, `score_5` (scores par niveau)
    - `score` (score total)

- Latitude/Longitude :
    - `lat_min`, `lat_max`, `lat`
    - `lng_min`, `lng_max`, `lng`

## 2. Dimensions

### A. Commandes

- `order_id` (identifiant de commande)
- `customer_id` (identifiant client)
- `status` (statut de la commande)

### B. Temps

- Dates principales :
    - `purchase_timestamp` (heure d'achat)
    - `approved_at` (date d'approbation)
    - `delivered_carrier` (date livraison transporteur)
    - `delivered_customer` (date livraison client)
    - `estimated_delivery` (date estimée de livraison)

- Découpages temporels :
    - `annee`, `mois`, `annee_mois`, `jour`, `annee_jour`
    - `jour_semaine`, `trimestre`, `annee_trimestre`
    - `semaine`, `annee_semaine`, `heure`

### C. Paiements

- `answer_1`, `answer_2`, `answer_3`, `answer_4`, `answer_5` (réponses spécifiques)
- `answer` (réponse globale)
- `comment_1`, `comment_2`, `comment_3`, `comment_4`, `comment_5` (commentaires spécifiques)
- `comment` (commentaire global)
- `creation_1`, `creation_2`, `creation_3`, `creation_4`, `creation_5` (créations spécifiques)
- `creation` (création globale)

### D. Clients

- `customer_unique_id` (identifiant unique client)
- `zip_code` (code postal client)
- `city` (ville client)
- `state` (état client)
- `name_state` (nom et état client)

## 3. Hiérarchies

### A. Temps

1. Hiérarchie annuelle :
    - `annee` > `trimestre` > `mois` > `jour` > `heure`
2. Hiérarchie hebdomadaire :
    - `annee` > `semaine` > `jour_semaine`

### B. Localisation

1. Latitude/Longitude :
    - `lat_min`, `lat_max`, `lat`
    - `lng_min`, `lng_max`, `lng`
2. Hiérarchie géographique :
    - `state` > `city` > `zip_code`

### C. Commande

- `order_id` > `customer_id`

### D. Paiements et interactions

- `creation` > `answer` > `comment` > `score`
