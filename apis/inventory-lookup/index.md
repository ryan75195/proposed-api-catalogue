# Inventory Lookup

Catalogues show stock as a single number, but availability really depends on warehouse, channel reservation and buffer. Merchants and shoppers get conflicting answers.

Inventory Lookup resolves available quantity for an SKU across warehouses and reservation pools. A call to GET /inventory/{sku}?warehouse=uk-east returns { "sku": "SW-12", "available": 38, "reserved": 12, "perWarehouse": { "uk-east": 38 } }.

Limits: it reflects data it is given and computes net availability only for warehouses it knows. It does not reserve stock or trigger replenishment.

This is a proposed design and is not implemented.

Available is intended as net-of-reservations and buffer, so a warehouse that is physically holding stock can still report low availability. Replenishment and allocation are out of scope.

A typical caller is the catalogue service that renders an add-to-cart button only when availability is positive. Per-warehouse detail lets a picker decide where an order should be fulfilled.

Warehouses that are not registered are simply omitted from the per-warehouse breakdown rather than assumed empty.
