# Updates via RabbitMQ

Updates are delivered through **RabbitMQ**.

## Connection

- Protocol: AMQP 0.9.1  
- Host: `rabbit.example.com`  
- Port: `5672`  
- VHost: `/feed`  
- Username/Password: provided by support  

## Exchange

- `feed.exchange` (type: `topic`)  

## Routing Keys

- `soccer.event.update`  
- `basketball.event.update`  
- `tennis.event.update`  
- `soccer.player.update`, etc.  

## Message Format

Example JSON:

Headers:

```
bid: 2
op: U
```

Message:
```json
{
  "id": "34694653",
  "date": 1757357100000,
  "eventId": 56418485,
  "bookmaker": 2,
  "sportId": 1,
  "players": {
    "7016132": {
      "id": "7016132",
      "name": "John Souttar",
      "shortName": "John Souttar",
      "fullName": "John Souttar",
      "markets": {
        "Goalscorers": {
          "#": {
            "1st": {
              "odd": 110,
              "updt": 1757322314457,
              "bSelectionId": "7016132",
              "bMarketId": "1.247409086",
              "marketTV": 48,
              "runnerTV": 0
            }
          }
        }
      },
      "team": null
    },
    "12977768": {
      "id": "12977768",
      "name": "Scott McTominay",
      "shortName": "Scott McTominay",
      "fullName": "Scott McTominay",
      "markets": {
        "Goalscorers": {
          "#": {
            "1st": {
              "odd": 75,
              "updt": 1757322314457,
              "bSelectionId": "12977768",
              "bMarketId": "1.247409086",
              "marketTV": 48,
              "runnerTV": 43
            }
          }
        }
      },
      "team": null
    }
  }
}
```
