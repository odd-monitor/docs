# Autenticazione & Sicurezza

- L’accesso al servizio è basato su **whitelist IP**.
- Non è richiesta API key o Bearer Token.
- Le chiamate da IP non autorizzati ricevono `403 Forbidden`.

## Rate Limit
- Lato API REST: 100 richieste/minuto per IP.
- Lato RabbitMQ: nessun limite, ma è raccomandata una sola connessione persistente per cliente.
