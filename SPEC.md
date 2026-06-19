# Restaurant Order Management System — Spec

## Hardware & software requirements
Mobile / tablet app on Android or iOS for **Waiter** — eases table allocation to customer details received from **Shift Manager** or **System Admin**.

The waiter can:
- Add or edit a table for a customer (table number, or keep in wait list)
- Once allocated, select menu items in the tablet
- Add notes from the customer
- Click **Submit Order** to send to kitchen

## Wireframe UI explanation

### Pre-conditions
1. Waiter is successfully logged in with credentials.
2. Customer is assigned to waiter via notification.
3. Tapping the notification selects the table; clicking **Proceed to Order** opens the order screen on the tablet / mobile app.

### Order entry screen fields
| Element | Behaviour |
|---|---|
| **Customer name + details** | Auto-populated from assignment data |
| **Table selection** | Dropdown of available tables |
| **Menu item search** | Type-ahead search; select from dropdown |
| **Item count** | Quantity selector per item |
| **Order list** | Items added by the customer; review before submission |
| **Submit** | Sends order to kitchen for preparation |
| **Previous** | Go back |

## Notes
> Detailed flow can be improved based on priority from stakeholders.

## Today's lens
A modern take would add: voice-driven order capture, allergen detection from menu LLM, dynamic upsell suggestions, kitchen-load-aware ETA, and a Stripe / payments gateway with split-bill — orchestrated as agents with eval-gated handoffs.
