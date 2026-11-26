# Aarish Co. + Aarish Jewelry

Static, responsive multi-brand storefront for:

- **Aarish Co.** — premium men's clothing.
- **Aarish Jewelry** — everyday jewellery.

The project keeps the existing HTML/CSS/JavaScript/Supabase stack. It includes a mixed-brand cart, cash-on-delivery checkout, owner authentication, separate product workflows, image uploads, inventory, order filtering, and server-side checkout price validation.

## Security notes

- Public users can read only available products, public settings, categories, and images.
- Customers do not receive direct order-table access; checkout runs through the `place_order` security-definer RPC.
- The RPC recalculates current sale/regular prices and validates availability before creating order items. It stores each item's brand.
- Only users listed in `store_owners` can manage products, images, inventory, settings, and orders.
- Cash on delivery is the only payment method; the UI does not claim an online payment succeeded.
