# Supply-Chain-Handling
The Real-World Problem: In e-commerce and logistics, when a shipment is delayed past its SLA or arrives damaged, operations teams manually jump across three systems—Order Management, Warehouse Inventory, and Ticketing/Refunds—to decide whether to reship or refund. This agent automates that entire triage workflow using 3 deterministic tool calls.
# Order Issue Handler

A simple tool-calling application built with Python, the Google GenAI SDK, and Gradio to automate e-commerce order exception handling.

## Problem Statement
When a customer reports a delayed or damaged order, support teams normally check three separate systems—order status, warehouse inventory, and ticketing—before deciding whether to reship or refund. This project automates that workflow using three Python tools and logs every run to a CSV file.

## Tools Used
1. **`get_order(order_id)`** — Looks up order details, item code, delivery status, and whether the order is past due.
2. **`check_stock(item)`** — Checks available inventory across Mumbai, Hyderabad, and Bengaluru warehouses.
3. **`log_action(order_id, action, note)`** — Records the final action (`reship`, `refund`, or `escalate`) and returns a ticket ID.

## Project Files
- `order_agent.ipynb` (or `.py`) — Main script with the 3 tools, decision rules, CSV logger, and Gradio UI.
- `order_agent_output.csv` — Automatically generated log of all queries, tool calls, and final replies.
- `README.md` — Project documentation.

## Setup & How to Run

1. Install the required packages:
   ```bash
   pip install google-genai gradio
