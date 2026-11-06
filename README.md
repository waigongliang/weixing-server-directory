# WeiXing Server Directory

Public endpoint directory used by the WeiXing client after its built-in server
cannot be reached.

## Updating endpoints

Edit `servers.json`. Keep `version` set to `1`, list no more than 12 origins,
and put the preferred endpoint first. Each origin must serve `GET /health` and
return JSON containing `{"status":"ok"}`.

Only endpoints backed by the same production account and message database may
be listed. Never place credentials, tokens, keys, or internal notes here.
