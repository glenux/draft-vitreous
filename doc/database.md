# Database model

## Entities

### User

| Name   | Type           | Description                   |
| ------ | -------------- | ----------------------------- |
| `id`   | `UUID`         | Internal identifier           |
| `role` | `VARCHAR(250)` | User role (`admin` or `user`) |

### Url

| Name       | Type     | Description                         |
| ---------- | -------- | ----------------------------------- |
| source_url | TEXT     | Original URL                        |
| short_id   | TEXT     | Short identifier                    |
| created_at | DATETIME | When this short URL was create      |
| expires_at | DATETIME | When this short URL must be deleted |

## Relations

### UserManagesUrls

* This relation has no properties
* `User` has many `Url`
