# HTTP Routes

| Verb   | Route                                | Method                   | Authenticated |
| ----   | ------------------------------------ | ------------------------ | ------------- |
| GET    | `/:short_id`                         | `root_short_url`         | No            |
| GET    | `/info`                              | `root_info`              | No            |
| GET    | `/api/v1/short-urls/`                | `short_urls_col_list`    | Yes           |
| POST   | `/api/v1/short-urls/`                | `short_urls_col_create`  | Yes           |
| GET    | `/api/v1/short-urls/stats`           | `short_urls_col_stats`   | Yes           |
| GET    | `/api/v1/short-urls/:short_id`       | `short_urls_item_read`   | Yes           |
| DELETE | `/api/v1/short-urls/:short_id`       | `short_urls_item_delete` | Yes           |
| UPDATE | `/api/v1/short-urls/:short_id`       | `short_urls_item_update` | Yes           |
| GET    | `/api/v1/short-urls/:short_id/stats` | `short_urls_item_stats`  | Yes           |

