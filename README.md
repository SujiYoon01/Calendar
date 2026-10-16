  td.cur-month:not(.chip-cell) { background-image: linear-gradient(to right, transparent var(--wk-a, 0%), color-mix(in srgb, var(--accent-biz) 14%, transparent) var(--wk-a, 0%), color-mix(in srgb, var(--accent-biz) 14%, transparent) var(--wk-b, 100%), transparent var(--wk-b, 100%)); }
  td.chip-cell.cur-month { background-image: linear-gradient(to right, transparent var(--wk-a, 0%), color-mix(in srgb, var(--accent-biz) 20%, transparent) var(--wk-a, 0%), color-mix(in srgb, var(--accent-biz) 20%, transparent) var(--wk-b, 100%), transparent var(--wk-b, 100%)); }
  .wk-strip { display: flex; gap: 2px; margin-top: 4px; }
  .wk-strip i { flex: 1; height: 4px; border-radius: 2px; background: color-mix(in srgb, var(--accent-biz) 25%, transparent); }
  .wk-strip i.on { background: var(--accent-biz); }

