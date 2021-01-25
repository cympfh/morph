# items

| id  | name | description | created  |
| INT | TEXT | TEXT        | DATETIME |

# transitions

The States after each transitions.

| at       | id  | state                            | level |
| DATETIME | INT | {"TODO", "WIP", "DONE", "ABORT"} | INT   |
