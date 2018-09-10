---
pagename: Des informations sur API
description: Des informations sur API de "Discord Fork"
lang: fr
---

# API Reference
Discord Fork is built on top of GitHub using GitHub pages and Jekyll, which means it is limited by GET requests only.
Please interface with the GitHub API in order to automate actions with the bot list.

**For other languages, prefix the link with `/:language`; For example: `/fr/api/bots/305277118105911296.svg`**

GET `/fr/api/:type/all.json`  
Obtain information on all `bots`, `servers` or `docs`

GET `/fr/api/:type/:id.json`  
Obtain information on a specific ID

The following is an example of `/api/bots/195244363339530240.json`.
`all.json` is an array of the the data below.

```json
{
  "draft": false,
  "categories": [

  ],
  "layout": "item",
  "type": "bots",
  "lang": "fr",
  "primary_key": "client_id",
  "client_id": "195244363339530240",
  "application_id": "195244341038546948",
  "pagename": "KawaiiBot",
  "description": "A kawaii Discord bot that makes your server more fun!",
  "avatar": "https://cdn.discordapp.com/avatars/195244363339530240/ec4594ead877809a2a53bade17f3cc94.png",
  "link": "https://discordapp.com/oauth2/authorize?client_id=195244341038546948&scope=bot",
  "github": {
    "owner": "KawaiiBot",
    "repo": "KawaiiBot"
  },
  "prefix": "+",
  "nsfw": false,
  "title": "195244363339530240",
  "slug": "195244363339530240",
  "ext": ".md",
  "tags": [

  ],
  "excerpt": "<p>KawaiiBot is a cute girl that aims to make your server more fun to be on!<br />\nPacked with fun commands like: hug, kiss, slots, coinflip, weather, time, and more!</p>\n\n",
  "permalink": "/bots/195244363339530240/"
}
```

Important mandatory fields:

Fields                 | Optional? | Description
---------------------- | --------- | -----------
lang                   | false     | The language of the page
primary_key            | false     | A reference to the actual key with the primary data.<br>For example, if `primary_key="client_id"`, the unique data is `client_id`
permalink              | false     | A link to the English version of the graphical page.<br>Prepend with `/:language` for other languages.

GET `/fr/api/:type/:id.svg`
Grab a fancy embed

`/fr/api/bots/305277118105911296.svg`  
![Un exemple avec le français de Homer](/fr/api/bots/305277118105911296.svg)

`/fr/api/docs/api-reference.svg`  
![An embed containing a self-description of this current page](/fr/api/docs/api-reference.svg)

`/fr/api/servers/330777295952543744.svg`  
![An embed for the Terminal.ink Discord Server](/fr/api/servers/330777295952543744.svg)

GET `/fr/api/:type/keys.json`  
Get all primary keys for the category.
