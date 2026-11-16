# Changelog

Tutte le modifiche rilevanti a questo modulo sono documentate in questo file.

Il formato è basato su [Keep a Changelog](https://keepachangelog.com/it/1.1.0/)
e questo progetto aderisce al [Semantic Versioning](https://semver.org/lang/it/).

## [1.0.0] - 2026-11-14

### Added
- Griglia **Negozi > Inventario > Quantità riservate**: quantità riservata da MSI per SKU e stock, ordini che la
  trattengono con stato e quantità, quantità bloccata su ordini completati, chiusi, annullati o non trovati.
  Ricerca, filtri, link a prodotto, ordini e (con `MageOS_InventoryReservationsGrid`) ai singoli movimenti.
- Colonna **Quantità riservata** nella griglia prodotti, con link agli ordini.
- ACL `Threecommerce_ReservedQty::view`, traduzioni `it_IT` e `en_US`.
