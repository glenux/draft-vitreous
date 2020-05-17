## Create short URL

### Request

`POST /api/v1/short-urls/`

| Parameter | Description            |
| --------- | ---------------------- |
| url       | original url           |
| ttl       | time to live (in days) |

Request example

```json
{
  "sourceUrl": "https://example.com",
  "expiresAt": "2020-05-17 12:34:12+02:00"
}
```

### Reponse

| Parameter    | Description                        |
| ------------ | ---------------------------------- |
| `id`         | unique id                          |
| `source_url` | original url                       |
| `created_at` | time to live, in days (0=infinite) |
| `expires_at` | time to live, in days (0=infinite) |

Response example

```json
{
  "result": "success",
  "shortUrl": {
    "sourceUrl": "https://example.com/super-long-url?with=shittons&of=paramters",
    "shortUrl": "https://exam.pl/sAQzTtx",
    "expiresAt": "2020-05-17 12:34:12+02:00"
  }
}
```

## Delete short URL

### Request

`DELETE /api/v1/short-urls/`

| Parameter   | Description  |
| ----------- | ------------ |
| `short_url` | original url |

Request example

```json
{
  "shortUrl": "https://exam.pl/sAQzTtx",
}
```

### Response

| Parameter  | Description  |
| ---------- | ------------ |
| `shortUrl` | original url |

Response example

```json
{
  "result": "success"
  "shortUrl": {
    "sourceUrl": "https://example.com/super-long-url?with=shittons&of=paramters",
    "shortUrl": "https://exam.pl/sAQzTtx",
    "expiresAt": "2020-05-17 12:34:12+02:00"
  }
}
```

## List all short URL

### Request

`GET /api/v1/short-urls/`

| Parameters      | Description   |
| --------------- | ------------- |
| `expiresAfter`  | Date included |
| `expiresBefore` | Date included |

### Response

Response example

```json
{
  "result": "success"
  "shortUrls": [
    {
      "sourceUrl": "https://example.com/super-long-url?with=shittons&of=paramters",
      "shortUrl": "https://exam.pl/sAQzTtx",
      "expiresAt": "2020-05-17 12:34:12+02:00"
    },
    {
      "sourceUrl": "https://example.com/super-long-url?with=shittons&of=paramters",
      "shortUrl": "https://exam.pl/oiTeRqW",
      "expiresAt": "2020-05-17 12:34:12+02:00"
    },
    // ...
  ]
}
```
