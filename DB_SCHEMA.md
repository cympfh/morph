# items

| id  | name | description | created  |
| INT | TEXT | TEXT        | DATETIME |

# transitions

The States after each transitions.

| tid | at       | id  | state                            | level |
| INT | DATETIME | INT | {"TODO", "WIP", "DONE", "ABORT"} | INT   |
