---
title: 'Flag 6: delete'
nav_order: 60
---

# Create a link that deletes users' files

_Difficulty:_ Medium

For convenience, UnicornBox allows you to quickly and easily delete all the
files you have in your account, with the click of a single button.  As an
attempt to remain secure, they have made sure that only POST requests will
actually delete the files---GET requests will not succeed.  In addition, they
have implemented a cross-origin resource sharing (CORS) policy that denies POST
requests from any external origin. This means that POST requests to delete all
files only succeed if they originate from the UnicornBox website.

**Your task:** Create a link that deletes user's files. Once you have figured it
out, execute the attack on yourself to earn the flag!

Note that this link must work for any logged in user, not just yourself.  In
other words, you must be able to email or text this link to someone else, and
when they click the link, their files are immediately deleted.

_Tip:_ To make a POST Request in JavaScript, use this line of code:

```
fetch('[URL]',{method:'POST'})
```

Note that there is no semicolon at the end. For example, to make a POST request
to `auth.berkeley.edu`, you would run the following JavaScript:

```
fetch('https://auth.berkeley.edu/',{method:'POST'})
```
