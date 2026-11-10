# Acceptance Criteria

**US-01 Login**
- Given a valid mobile number, when I request an OTP, then an OTP is sent and valid for 5 minutes.
- Given a correct OTP, then I am logged in; given a wrong OTP, then an error shows and I can retry up to 3 times.

**US-02 Search**
- Given I enter a keyword, then restaurants matching name or cuisine within delivery range are listed.
- Given nothing matches, then a "no restaurants found" message appears.

**US-03 Menu**
- Given I open a restaurant, then items show name, price, description and veg/non-veg tag.
- Given an item is unavailable, then it is shown as unavailable and cannot be added.

**US-04 Cart and promo**
- Given I add items, then the cart total includes taxes and fees.
- Given I apply a valid promo code, then the discount shows; given an invalid or second code, then an error shows.

**US-05 Place order**
- Given my cart meets the minimum order value, when I choose an address within 8 km, then I can proceed to payment.
- Given the address is outside 8 km, then a "not deliverable" message appears.

**US-06 Payment**
- Given I pay by UPI or card successfully, then the order is confirmed and a receipt is shown.
- Given payment fails, then I see the reason and can retry without rebuilding the cart.
- Given I choose cash on delivery, then the order is confirmed with payment pending.

**US-07 Restaurant response**
- Given a new order, then the restaurant sees it with a 3-minute response timer.
- Given no response in 3 minutes, then the order is auto-cancelled and the customer notified and refunded if paid.

**US-08 Tracking**
- Given the order status changes, then the customer gets a notification and the status updates in the app.
- Given a delivery partner is assigned, then their name and live location are shown.

**US-09 Cancel**
- Given the restaurant has not started preparing, when I cancel, then the order is cancelled and refunded as per BR-6.
- Given preparation has started, then cancel is not allowed and a message explains why.

**US-10 Rating**
- Given the order is delivered, then I can give 1–5 stars and an optional comment up to 300 characters.
- Given I have already rated, then I cannot rate the same order again.
