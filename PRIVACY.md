# Privacy Policy — Daycare Photos

Last updated: October 3, 2026

## What this is

"Daycare Photos" is a personal Google Apps Script used by its author and no one
else. It moves photos from daycare report emails in the author's Gmail into the
author's own Google Photos library.

It is not a product, it is not offered to other people, and it has no users
besides the author.

## What it accesses

With the author's own Google authorization, the script:

- **Reads Gmail messages** from the daycare's sending domain, in order to find
  the photos in them (`gmail.readonly`).
- **Adds photos to Google Photos** (`photoslibrary.appendonly`). This permission
  is append-only: the script can upload new photos but cannot read, modify or
  delete anything already in the library.
- **Downloads images** from the URLs the daycare's emails point to
  (`script.external_request`).
- **Creates a recurring timer** so it can run on a schedule
  (`script.scriptapp`).

## Where data goes

Nowhere. The script runs on Google's Apps Script infrastructure inside the
author's own Google account. Email contents and photos move from the author's
Gmail to the author's Google Photos and are not sent, copied, sold, shared or
disclosed to any third party, service or person.

There is no server, no database, and no analytics. No developer other than the
author has access.

## What is stored

Only bookkeeping, held in the script's own properties inside the author's Google
account:

- IDs of emails already processed, so they are not handled twice.
- MD5 fingerprints of photos already uploaded, so duplicates are skipped.
- The ID of the Google Photos album the script created.

No email bodies, no photos and no personal information are retained. These
entries are deleted automatically after 120 days.

## Data retention and deletion

Photos uploaded to Google Photos are the author's own and are governed by
Google's terms. They can be deleted directly in Google Photos at any time.

Access can be revoked at any time at
<https://myaccount.google.com/permissions>, which stops the script immediately.

## Children's data

The photos are of the author's own children, handled by the author alone, and
are never disclosed to anyone. No information about any child is collected,
transmitted or shared.

## Changes

Any change to this policy will be committed to this repository, where the
revision history is public.

## Contact

Open an issue on this repository.
