## 2026-02-01 - [Optimizing Periodic Tasks and UART Processing]
**Learning:** Replacing modulo (%) with comparison/reset logic significantly reduces CPU overhead on Cortex-M3, which lacks a single-cycle hardware divider. Handling circular buffer wrap-around manually is safer and faster.
**Action:** Always prefer conditional wrap-around checks over modulo for fixed-size buffers and periodic interrupts.
