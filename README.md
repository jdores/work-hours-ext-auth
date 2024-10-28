# External Auth example worker

This workers uses the [base code to set up an external evaluation in Cloudflare Access](https://developers.cloudflare.com/cloudflare-one/policies/access/external-evaluation/) and adds the logic so that it returns true for an access attempt that happened during business hours and a returns false if that attempt happens outside of business hours.

The time evaluation is local to the location from here the access attempt is done (an access attempt from Lisbon will consider the Lisbon timezone, while an access attempt from Tokyo will consider the Tokyo timezone).

The business hours and days are set in wrangler.toml