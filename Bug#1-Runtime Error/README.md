## BUG #1 — Missing InputGroup Import (Runtime Crash)
<img width="927" height="97" alt="image" src="https://github.com/user-attachments/assets/32243075-8674-41e5-aea1-fda4c05744a3" />
<img width="930" height="247" alt="image" src="https://github.com/user-attachments/assets/69e91451-581d-4df3-a33f-ddb48de1cafc" />

## Explanation:
InputGroup is used in the JSX at lines 196 and 248, but is never imported from react-bootstrap. This will cause a ReferenceError: InputGroup is not defined at runtime whenever the cashier modal renders. The cashier open/close functionality is completely broken.

## Real-world impact:
Cashier cannot open or close their register — core POS functionality is blocked.




