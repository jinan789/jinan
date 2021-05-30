---
title: 'Flag 4: nicholas'
nav_order: 40
---

# Gain access to `nicholas`'s account

_Difficulty:_ Hard

UnicornBox uses token-based authentication. The database stores a table that
maps session tokens to users:

```
CREATE TABLE IF NOT EXISTS sessions (
    username TEXT,
    token TEXT,
    -- Additional fields not shown.
);
```

Whenever an HTTP request is received, the server checks for a `session_token`
value in the cookie. If the cookie contains a token, the server selects the
username corresponding to that token from the `sessions` table.

**Your task:** Gain access to `nicholas`'s account.

_Tip:_ Cookie values may contain anything other than semicolons, which are used
as delimiters in cookie syntax.
