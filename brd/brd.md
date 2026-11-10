# Business Requirements Document (BRD)

*Sample document for a fictional product. Version 1.0*

## 1. Purpose
Define what the food-delivery application must do so that customers can order meals from partner restaurants and receive them reliably.

## 2. Business objectives
| ID | Objective |
|---|---|
| BO-1 | Let a customer find food and place a paid order in under 3 minutes. |
| BO-2 | Give restaurants a simple way to receive and manage orders. |
| BO-3 | Give customers live visibility of their order status. |
| BO-4 | Reduce order disputes through clear cancellation and feedback rules. |

## 3. Scope
**In scope:** customer registration and login, restaurant search and menu, cart, promo codes, order placement, payment, restaurant order handling, delivery assignment, live tracking, cancellation, ratings.
**Out of scope:** restaurant onboarding, delivery-partner payouts, loyalty programme, multi-city expansion.

## 4. Stakeholders
| Stakeholder | Role / interest |
|---|---|
| Customer | Orders food; wants speed, accuracy and tracking |
| Restaurant partner | Receives and prepares orders |
| Delivery partner | Picks up and delivers orders |
| Operations / admin | Monitors orders, handles issues |
| Payment gateway | Processes payments |
| Product owner | Owns scope and sign-off |
| Development and QA teams | Build and test |

## 5. Functional requirements
| ID | Requirement | Priority | Objective |
|---|---|---|---|
| FR-01 | The system shall let users register and log in using a mobile number and OTP. | High | BO-1 |
| FR-02 | The system shall let users search restaurants by location, name and cuisine. | High | BO-1 |
| FR-03 | The system shall show each restaurant's menu with item name, price, description and veg/non-veg tag. | High | BO-1 |
| FR-04 | The system shall let users add, change and remove items in a cart and show the total including taxes and fees. | High | BO-1 |
| FR-05 | The system shall let users apply one valid promo code to an order. | Medium | BO-1 |
| FR-06 | The system shall let users place an order with a saved or new delivery address. | High | BO-1 |
| FR-07 | The system shall support payment by UPI, card and cash on delivery. | High | BO-1 |
| FR-08 | The system shall let restaurants accept or reject an incoming order. | High | BO-2 |
| FR-09 | The system shall assign an available delivery partner after the restaurant accepts. | High | BO-3 |
| FR-10 | The system shall show order status (accepted, preparing, picked up, delivered) and notify the user at each change. | High | BO-3 |
| FR-11 | The system shall let users cancel an order before the restaurant starts preparing it. | Medium | BO-4 |
| FR-12 | The system shall let users rate the food and delivery after delivery. | Low | BO-4 |

## 6. Non-functional requirements
- Pages and search results load within 3 seconds for 95% of requests.
- Payment data is handled by the payment gateway and not stored by the app.
- The app works on current Android and iOS versions.
- The system supports at least 5,000 concurrent users (assumption).

## 7. Business rules
| ID | Rule |
|---|---|
| BR-1 | Delivery is available only within 8 km of the restaurant. |
| BR-2 | A minimum order value of ₹100 applies. |
| BR-3 | Only one promo code can be applied per order. |
| BR-4 | An order can be cancelled only before the restaurant starts preparing it. |
| BR-5 | If the restaurant does not respond within 3 minutes, the order is auto-cancelled and any payment refunded. |
| BR-6 | Refunds go to the original payment method within 5–7 working days. |

## 8. Assumptions and constraints
- Restaurants and delivery partners are already onboarded.
- A third-party payment gateway and a maps service are available through APIs.
- Menu and price data is supplied by restaurants.

## 9. Risks
Restaurants not responding in time, payment gateway downtime, inaccurate delivery estimates.

## 10. Approval
Product owner: ____________ Date: ________
