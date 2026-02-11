## BUG #2 — Duplicate API Calls Wasting Resources
<img width="926" height="393" alt="image" src="https://github.com/user-attachments/assets/d466e80a-3f33-4a05-a392-e6555ee7d384" />

## Explanation:
Both APIs are called via Promise.all first (results stored in lowStockResponse1, zeroStockResponse1 — never used), 
then called again individually. This fires 4 HTTP requests instead of 2 — doubling server load and response time.

## Real-world impact:
Double load on the backend for every page visit. Slower page loading. Wasted bandwidth.
