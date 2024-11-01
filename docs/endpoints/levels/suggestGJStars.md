# suggestGJStars20.php

> Endpoint used by moderators to send levels to RobTop.

## Parameters

### Required Parameters

**accountID** - accountID of the user.

**gjp** - The [GJP](/topics/gjp.md) of the user.

**levelID** - the ID of the level

**stars** - How many stars that are requested.

**secret** - Wmfp3879gc3

**gameVersion** - the game version

**binaryVersion** - the binary version

**feature** - 0 for star rate, 1 for feature, 2 for epic, 3 for legendary, 4 for mythic.

**gdw** - 0

## Response

`-2` if not a moderator.
`1` if is a moderator.

## example

<!--tabs:start -->

## Python
```py
import requests

data = {
        "gameVersion": 21,
        "binaryVersion":35
        "accountID": 71, # a moderators accountID
        "gjp": "********", # This would be the mods password encoded with GJP encryption
        "levelID": 128,
        "stars": 3,
        "feature": 0,
        "gdw": 0,
        "secret": "Wmfp3879gc3"
}

req = requests.post("http://boomlings.com/database/suggestGJStars20.php", data=data)
print(req.text)

```

**Response**
```plain
1
```
