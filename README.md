# Daycare Photos

A personal Google Apps Script that files my kids' daycare photos automatically.

The daycare sends a daily report email with the day's photos in it. This script
watches for those emails in Gmail, pulls the photos out, and uploads them to an
album in my own Google Photos library. That's the whole thing.

It runs inside my own Google account on a 15-minute timer. There is no server,
no website, and no other user.

## How it works

1. Searches Gmail for new messages from the daycare.
2. Extracts the photos — both file attachments and images the email links to
   on the daycare's own server.
3. Filters out logos, spacer images and tracking pixels by size and URL.
4. Uploads what's left to a Google Photos album, skipping anything it has
   already uploaded.

## Permissions it uses

| Scope | Why |
|---|---|
| `gmail.readonly` | Read the daycare's emails to find the photos. |
| `photoslibrary.appendonly` | Add photos to my library. This scope cannot read existing photos. |
| `script.external_request` | Download the photos from the daycare's server. |
| `script.scriptapp` | Create the timer that runs the script. |

## Privacy

See [PRIVACY.md](PRIVACY.md). Short version: nothing leaves my own Google
account, and no data is collected or shared.
