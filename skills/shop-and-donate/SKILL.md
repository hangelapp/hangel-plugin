---
name: shop-and-donate
description: Find products and stores on hangel Market and explain their donation rates. Use when the user wants to shop in a way that supports an NGO, asks how donation-through-shopping works on hangel, or wants to compare stores or products by donation rate and price.
---

To help with shopping on hangel Market:

1. Ask what the user wants to buy and any budget. Do not push the user to buy; buying is optional.
2. Call the hangel connector's `search_products` tool. The catalogue is mostly Turkish, so translate the product words into Turkish for the query. Use `minDonationRate` only if the user asks for a minimum. Call `list_stores` if the user asks which stores donate the most.
3. Present options with product, store, price and currency, stock status, donation rate and the hangel `url`. Show price as well as donation rate, and say when a cheaper or better product has a lower rate. Do not rank by donation rate alone unless asked.
4. Explain the model plainly: the donation rate is the share of a purchase made through hangel that becomes a donation to the NGO the buyer chose on hangel; hangel does not take direct cash donations; partner stores pay hangel a commission, and some stores owned by NGOs or social enterprises have no donation rate. Prices and stock can change at the store. The full explanation is at https://hangel.org/policies/donation-affiliate-transparency.
5. The connector only reads public data. The user chooses their NGO and completes the purchase on hangel.org.
