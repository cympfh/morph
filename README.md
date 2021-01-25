# morph

Yet Another TODO management Tool

## CLI

### New Project

```bash
morph new <PROJECT_NAME>
```

A Project file (sqlite3 file) will be created at `~/.cache/morph/<PROJECT_NAME>`

DONT USE Special character `/` for `PROJECT_NAME`.
And `PROJECT_NAME` must be unique in your system.

### New Item

Append new item as TODO.

```bash
morph new <PROJECT_NAME>/<ITEM_NAME> [ --description DESCRIPTION ]
```

`ITEM_NAME` is freely text (but, DONT BEGIN with `@`).
Automatically, every items are given `ITEM_ID` which begin with `@`.

### Transition (TODO <-> IN_PROGRESS <-> DONE <-> ABORT)

```bash
morph mv <PROJECT_NAME>/<ITEM_NAME> <STATE>
morph mv <PROJECT_NAME>/<ITEM_ID> <STATE>
```

If `ITEM_NAME` is unique, you can use it.

```bash
STATE:
    TODO
    WIP
    DONE
    ABORT
```

### Progress Level

IN_PROGRESS Items have the **Progress Level**.
Initially it is `0`.

#### Increment level

```bash
morph inc <PROJECT_NAME>/<ITEM_NAME>
```

If the item is not IN_PROGRESS, this occurs an Error.

#### Done items

Use `morph mv`.

### List up Items

```bash
morph ls <PROJECT_NAME>
morph ls <PROJECT_NAME> [OPTIONS]
morph ls <PROJECT_NAME>/<ITEM_NAME>
morph ls <PROJECT_NAME>/<ITEM_ID>
```

```bash
OPTIONS:
    -s STATE
```

### Delete Item

Delete an item and its history completely.

```bash
morph rm <PROJECT_NAME>/<ITEM_NAME>
morph rm <PROJECT_NAME>/<ITEM_ID>
```

### Delete Project

Delete All Completely.

```bash
morph rm <PROJECT_NAME>
```

