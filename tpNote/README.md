# Liste des colonnes ajoutées avec hiérarchies, dimensions et métriques par DataFrame

## 1. **order_payments**

- **Hiérarchie :** Mode de paiement
- **Dimensions :**
    - `int_boleto` (nombre de paiements par boleto)
    - `int_credit_card` (nombre de paiements par carte de crédit)
    - `int_debit_card` (nombre de paiements par carte de débit)
    - `int_not_defined` (nombre de paiements indéfinis)
    - `int_voucher` (nombre de paiements par bon)
- **Métriques :**
    - `value_boleto` (montant total payé par boleto)
    - `value_credit_card` (montant total payé par carte de crédit)
    - `value_debit_card` (montant total payé par carte de débit)
    - `value_not_defined` (montant total payé via un mode indéfini)
    - `value_voucher` (montant total payé par bon)

---

## 2. **orders**

- **Hiérarchie :** Temps > Commandes
- **Dimensions :**
    - `annee` (année de la commande)
    - `mois` (mois de la commande)
    - `annee_mois` (année et mois combinés)
    - `jour` (jour de la commande)
    - `annee_jour` (année et jour combinés)
    - `jour_semaine` (jour de la semaine)
    - `trimestre` (trimestre de l'année)
    - `annee_trimestre` (année et trimestre combinés)
    - `semaine` (semaine de l'année)
    - `annee_semaine` (année et semaine combinées)
    - `heure` (heure de la commande)
    - `status` (statut de la commande)
- **Métriques :**
    - `approuvee` (date commande approuvée)
    - `envoyee` (date commande envoyée)
    - `livree` (date commande livrée)
    - `estimee` (date commande estimée livrée)
    - `jours_retard` (jours de retard de livraison)

---

## 3. **order_reviews**

- **Hiérarchie :** Commentaires > Temps
- **Dimensions :**
    - `answer_1`, `answer_2`, `answer_3`, `answer_4`, `answer_5` (temps de réponse pour les commentaires)
    - `comment_1`, `comment_2`, `comment_3`, `comment_4`, `comment_5` (textes des commentaires)
    - `creation_1`, `creation_2`, `creation_3`, `creation_4`, `creation_5` (dates de création des commentaires)
- **Métriques :**
    - `score_1`, `score_2`, `score_3`, `score_4`, `score_5` (notes des commentaires)
    - `score` (note globale)
    - `answer` (temps de réponse moyen)
    - `creation` (date de création moyenne des commentaires)
    - `comment` (commentaire moyen/récapitulatif)

---

## 4. **order_customers**

- **Hiérarchie :** Localisation > Clients
- **Dimensions :**
    - `zip_code` (code postal du client)
    - `city` (ville du client)
    - `state` (état du client)
    - `name_state` (nom de l'état du client)
    - `lat_min`, `lat_max`, `lat` (latitude du client - min, max, moyenne)
    - `lng_min`, `lng_max`, `lng` (longitude du client - min, max, moyenne)
- **Métriques :**
    - *(Aucune métrique supplémentaire)*

---

## 5. **geolocation**

- **Hiérarchie :** Localisation
- **Dimensions :**
    - *(Aucune colonne ajoutée identifiable ici)*

---

## 6. **products**

- **Hiérarchie :** Catégories > Produits
- **Dimensions :**
    - `name_lenght` (longueur du nom du produit)
    - `description_lenght` (longueur de la description du produit)
    - `photos_qty` (nombre de photos du produit)
    - `weight_g` (poids en grammes)
    - `length_cm` (longueur en cm)
    - `height_cm` (hauteur en cm)
    - `width_cm` (largeur en cm)
    - `category_name` (nom de la catégorie)
- **Métriques :**
    - *(Aucune métrique supplémentaire)*

---

## 7. **order_items**

- **Hiérarchie :** Commandes > Articles
- **Dimensions :**
    - `limit` (limite d'expédition)
- **Métriques :**
    - *(Aucune métrique supplémentaire)*

---

## 8. **sellers**

- **Hiérarchie :** Localisation > Vendeurs
- **Dimensions :**
    - `sell_zip_code` (code postal du vendeur)
    - `sell_city` (ville du vendeur)
    - `sell_state` (état du vendeur)
    - `sell_name_state` (nom de l'état du vendeur)
    - `sell_lat` (latitude du vendeur)
    - `sell_lng` (longitude du vendeur)
- **Métriques :**
    - *(Aucune métrique supplémentaire)*
