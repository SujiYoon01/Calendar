  .info-card {
    position: absolute; left: 50%; top: 50%; transform: translate(-50%, -50%);
    width: 90%; max-width: 420px; max-height: 60vh; overflow: auto;
    background: var(--surface); border-radius: 16px;
    padding: 26px 20px 18px; box-shadow: 0 12px 40px rgba(0,0,0,0.28);
    animation: info-card-pop .14s ease-out; cursor: grab;
  }
  .info-card.stack-1 { top: 2vh; bottom: auto; transform: translateX(-50%); max-height: 22vh; max-width: 320px; }
  .info-card.stack-2 { top: 4vh; left: 50%; margin-left: 30px; }
