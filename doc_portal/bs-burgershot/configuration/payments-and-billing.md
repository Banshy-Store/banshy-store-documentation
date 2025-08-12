# Payments & Billing

- `BSConfig.Payments.mode`:
  - 'direct': customer pays (cash/bank). Split by `share` → society + employee.
  - 'billing': ESX billing or qb-billing if installed. Otherwise falls back to direct with a notice.
- `BSConfig.Payments.share`: table with `society` and `employee` (must total 1.0).
