## BUG #7 — Global Namespace Pollution via window._handleHoldSalesKeyDown
<img width="922" height="403" alt="image" src="https://github.com/user-attachments/assets/4d2b7782-fcfc-4342-bd5d-3c374d02462a" />

## Solve Bug

<img width="822" height="675" alt="image" src="https://github.com/user-attachments/assets/ead61640-13a5-442c-b79b-90aca4242374" />

## Explanation:
Event listeners are stored on the window object and re-registered every time currentSale or holdSales changes. 
This: (1) pollutes the global namespace, (2) risks race conditions if multiple component instances exist, (3) creates a new listener on every state change.

## Real-world impact: 
Multiple redundant keyboard handlers pile up. Key presses may fire handlers multiple times. Memory leak grows with each sale change.
