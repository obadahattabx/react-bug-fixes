## BUG #6 — style jsx Used Without styled-jsx Plugin
<img width="925" height="300" alt="image" src="https://github.com/user-attachments/assets/5ce97870-3ed1-44a2-8511-ad97b05e3e08" />

## Solve Bug:

<img width="591" height="292" alt="image" src="https://github.com/user-attachments/assets/907473af-dcee-41fd-8ceb-82c894cbcc2e" />

## Explanation:
style jsx is a Next.js/styled-jsx feature. This Vite+React project doesn't have styled-jsx installed.
  The jsx attribute is silently ignored and the styles are injected as global CSS — not scoped as intended.
## Real-world impact:
  CSS is globally leaked, potentially causing style conflicts. The jsx attribute gives a false sense of scoping.
  
  
