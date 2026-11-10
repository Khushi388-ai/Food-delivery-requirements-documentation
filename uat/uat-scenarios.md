# UAT Scenarios

| ID | Scenario | Steps | Expected result | Story |
|---|---|---|---|---|
| UAT-01 | Login with valid OTP | Enter number, request OTP, enter OTP | Logged in | US-01 |
| UAT-02 | Login with wrong OTP | Enter wrong OTP 3 times | Error each time; blocked after 3 attempts | US-01 |
| UAT-03 | Search by cuisine | Search "biryani" | Matching restaurants in range listed | US-02 |
| UAT-04 | View menu with unavailable item | Open a menu | Unavailable item cannot be added | US-03 |
| UAT-05 | Apply valid promo | Add items, apply code | Discount applied to total | US-04 |
| UAT-06 | Apply second promo | Apply another code | Rejected with message | US-04 |
| UAT-07 | Order below minimum value | Cart under ₹100, checkout | Blocked with message | US-05 |
| UAT-08 | Address outside 8 km | Choose far address | "Not deliverable" message | US-05 |
| UAT-09 | Successful UPI payment | Pay by UPI | Order confirmed, receipt shown | US-06 |
| UAT-10 | Failed payment and retry | Fail payment, retry | Reason shown; retry works, cart kept | US-06 |
| UAT-11 | Restaurant no response | Do not respond for 3 minutes | Order auto-cancelled; refund triggered | US-07 |
| UAT-12 | Track order | Follow order to delivery | Status updates and notifications at each stage | US-08 |
| UAT-13 | Cancel before and after preparation | Cancel at both points | Allowed before, blocked after | US-09 |
| UAT-14 | Rate a delivered order | Rate 4 stars with comment | Saved; second rating blocked | US-10 |

**Exit criteria:** all scenarios passed, no open critical/high defects, product-owner sign-off.
