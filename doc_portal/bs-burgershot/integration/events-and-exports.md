# Events & Exports

Server events (namespace `bs-burgershot:*`):
- `cookItem`, `prepareDish`, `cutItem`, `prepareDrink`
- `newCustomerOrder`, `payOrder`, `billCustomer`
- `announceOpen`, `announceClose`

Client export:
- `exports['bs-burgershot']:OpenCustomerMenu()`

Legacy aliases are bridged server-side.
