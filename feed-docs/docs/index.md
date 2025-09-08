# Feed Quote Sportive

Questo servizio fornisce un **feed di quote** per:
- Calcio
- Basket
- Tennis

L’architettura prevede:
1. **Snapshot iniziale via API REST** (eventi, extra, player).
2. **Aggiornamenti in tempo reale via RabbitMQ**.

L’accesso è consentito **solo da IP in whitelist**.
