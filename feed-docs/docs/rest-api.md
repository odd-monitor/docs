# API REST - Snapshot

Le API REST sono esposte via HTTPS.

## Endpoint Principale
```
GET /snapshot/{product}/{sport}/{bookmaker}
```

### Parametri
- `product`: `events` | `extra` | `player`
- `sport`: `soccer` | `basketball` | `tennis`
- `bookmaker`: stringa identificativa del bookmaker

### Risposte
- **200 OK**: JSON con snapshot
- **400 Bad Request**: parametri invalidi
- **403 Forbidden**: IP non autorizzato

### Esempio
```bash
curl https://api.example.com/snapshot/events/soccer/bwin
```

### Documentazione Interattiva
- Swagger UI: [https://api.example.com/docs](https://api.example.com/docs)
- OpenAPI JSON: [https://api.example.com/openapi.json](https://api.example.com/openapi.json)
