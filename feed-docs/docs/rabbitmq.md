# Aggiornamenti via RabbitMQ

Gli aggiornamenti sono inviati tramite **RabbitMQ**.

## Connessione
- Protocollo: AMQP 0.9.1
- Host: `rabbit.example.com`
- Porta: `5672`
- VHost: `/feed`
- Utente/password: forniti dal supporto

## Exchange
- `feed.exchange` (tipo: `topic`)

## Routing Keys
- `soccer.event.update`
- `basketball.event.update`
- `tennis.event.update`
- `soccer.player.update`, ecc.

## Formato Messaggi
Esempio JSON:
```json
{
  "event_id": "12345",
  "bookmaker": "bwin",
  "market": "1x2",
  "odds": {
    "home": 1.85,
    "draw": 3.20,
    "away": 4.50
  },
  "timestamp": "2025-09-05T12:30:00Z"
}
```
