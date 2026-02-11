## BUG #5 — Hardcoded localhost URLs Bypassing API Service
<img width="935" height="308" alt="image" src="https://github.com/user-attachments/assets/730eac08-4fa2-410b-b15f-09cf30cdbb1e" />

## Solve Bug:
<img width="696" height="367" alt="image" src="https://github.com/user-attachments/assets/ee20ce96-42cb-4ad9-b0cf-d5c201ce0dd7" />

## Explanation:
Uses raw fetch() with http://localhost:3005 instead of the api service. These calls: (1) won't work in production,
(2) bypass the auth interceptor so requests go out without tokens, (3) contain a likely typo invalidProce instead of invalidPrice.


## Real-world impact:
 Entire page is non-functional in production. Auth bypass. Endpoint typo.
