## BUG #3 — Redirect to Non-Existent
<img width="921" height="366" alt="image" src="https://github.com/user-attachments/assets/fba2896a-2ec4-47be-a723-0fad5d0da1bb" />

## Explanation:
When the token is invalid, the user is redirected to /logout, but no /logout route exists in App.jsx. 
This will result in either a blank page (caught by the wildcard /* route showing Dashboard — which itself requires auth) or an infinite redirect loop.

## Real-world impact:
Users with expired tokens see a broken/blank page instead of being redirected to login. They cannot recover without manually clearing localStorage.
