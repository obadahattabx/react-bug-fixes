## BUG #4 — salesreturn Route is Unprotected

<img width="921" height="325" alt="image" src="https://github.com/user-attachments/assets/7af4d921-3011-491c-b8b5-d0a84d3a40c9" />

## Solve Bug :
<img width="965" height="582" alt="image" src="https://github.com/user-attachments/assets/537f04dd-f2c6-4643-811f-1ccde6ec0f87" />

## Explanation:
The salesreturn route is placed outside the <ProtectLogin> wrapper, meaning anyone can access the sales returns page without authentication.
This page allows refunding sales.

## Real-world impact:
Unauthenticated users can perform sales refunds, causing financial loss and inventory corruption.
