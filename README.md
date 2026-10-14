# Vic Park HA Lab

"Make Your Own HA" booth form for Renellence at the Vic Park Medispa Convention.

- `index.html` — the whole site (plain HTML/CSS/JS, no build step), rebuilt from the Claude Design file
  `Make Your Own HA.dc.html` with the same layout, wording and colours.
- The form posts to the n8n webhook `vic-park-ha-lab` (a branch of the `[REG] Liberty Grand RSVP` workflow),
  which writes one row per registration to the Google Sheet **Vic Park HA Lab Registrations** and emails
  info@renellence.com if a row cannot be saved. The webhook only accepts requests from this site's address.
- Bots are screened the same way as the launch RSVP: a hidden "company website" field and a minimum time to fill in.

Code: https://github.com/Info-Renellence/vic-park-ha-lab. Vercel project `vic-park-ha-lab` deploys every push to `main` to https://vic-park-ha-lab.vercel.app.
