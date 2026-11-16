# Threecommerce_ReservedQty: MSI reserved quantities in the Magento 2 / Mage-OS admin

With MSI (Multi-Source Inventory) Magento does not lower the stock when an order comes in: it **reserves** the quantity and takes it off the salable quantity until the order is shipped, canceled or refunded. The admin never shows what is reserved or by which orders, only that the salable quantity is lower than the stock. This module shows it, and finds the quantities left **stuck** on orders that are already closed.

![Reserved Quantities grid: reserved quantity per SKU and stock, orders holding it, stuck quantity](images/reserved-qty-grid.png)

**Compatibility:** Magento Open Source / Adobe Commerce 2.4.4 – 2.4.9 · Mage-OS 1.x / 3.x / 4.x · PHP 8.1 – 8.4 · MSI enabled
**License:** commercial · coming soon

## Features

- **Stores → Inventory → Reserved Quantities**: one row per SKU and stock with the quantity still reserved, linked to the product.
- The **orders holding the quantity**, each with a link, its status and its quantity.
- **Stuck quantity**: what is still reserved by complete, closed or canceled orders, by orders that no longer exist or by reservations without an order. These quantities lower the salable quantity for no reason; the core commands `inventory:reservation:list-inconsistencies` and `inventory:reservation:create-compensations` fix them.
- Keyword search on SKU and name, filters on stock and on quantity ranges, sorting on every number.
- A **Reserved Quantity** column in the product grid, next to Salable Quantity, with a link to the orders of that SKU.
- On Mage-OS, a link from each row to the single reservation movements in the native *Reservations* grid.
- Read only: it never creates, changes or deletes reservations. Own ACL resource for admin roles.

![Product grid with the Reserved Quantity column next to Salable Quantity](images/reserved-qty-product-grid.png)

![The single reservation movements of a SKU in the Mage-OS Reservations grid](images/reserved-qty-movements.png)

## Requirements

- Magento Open Source / Adobe Commerce 2.4.4+ or Mage-OS
- PHP 8.1 or newer, MySQL 5.7+ or MariaDB 10.2.3+
- MSI enabled: `Magento_InventoryReservations`, `Magento_InventoryAdminUi`
- Package: `threecommerce/m2-base`

## Availability

This module is **not yet available to buy**. It is a commercial product and is coming soon. To be notified when it is released, or to ask for details, [get in touch](https://www.threecommerce.it/contatti?utm_source=github&utm_medium=readme&utm_campaign=magento2-reserved-qty).

## Configuration

None: after `bin/magento setup:upgrade` the grid is in the Stores → Inventory menu and the column is in the product grid. Access is granted per admin role with the *Reserved Quantities* resource.

## Documentation and support

- [Changelog](CHANGELOG.md)
- Support and custom development: [threecommerce.it/contatti](https://www.threecommerce.it/contatti?utm_source=github&utm_medium=readme&utm_campaign=magento2-reserved-qty)

---

*This repository is the public showcase of the module. The source code is kept in a private repository.*
