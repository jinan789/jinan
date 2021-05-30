---
title: 'Flag 3: shomil'
nav_order: 30
---

# Obtain `shomil`'s password hash

_Difficulty:_ Medium

The UnicornBox database uses the following table `users` to store its accounts:

```
CREATE TABLE IF NOT EXISTS users (
    username TEXT,
    md5_hash TEXT,
    -- Additional fields not shown.
);
```

**Your Task:** Steal the password hash for user `shomil`.

_Tip:_ You may execute multiple statements in one line separated by semicolons
in SQL, but it will only return the results of the last query if it does not
have a semicolon.

```
SELECT '123'; SELECT '456' -- returns '456'
SELECT '123'; SELECT '456'; -- returns nothing
```
