# So Cal Athletics James/Brown 28 Premier — Team Site

A Jekyll site for the 16U travel softball team: landing page, full roster with
individual player profiles, and a tournament schedule.

## Publishing to GitHub Pages

1. Create a new **public** GitHub repository (e.g. `socal-athletics-28-premier`).
2. Push all these files to the `main` branch.
3. In the repo, go to **Settings → Pages**, set Source to "Deploy from a branch",
   branch `main`, folder `/ (root)`. Save.
4. Your site will publish at `https://<your-username>.github.io/<repo-name>/`.
5. Open `_config.yml` and set `url` to that address and `baseurl` to
   `/<repo-name>` (leave `baseurl` blank if this is a `username.github.io` repo).

GitHub automatically rebuilds the site every time you push a change — no
extra build step needed.

## Testing changes locally (optional)

If you want to preview edits before pushing:

```
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000` in a browser.

## How to update things

### Add or edit a game / tournament
Edit `_data/schedule.yml`. Copy an existing tournament block (starting with
`- name:`) to add a new one, or add a new game under `games:` in an existing
tournament. Fill in `result:` (e.g. `"W 8-2"`) once a game is played and it
will show automatically.

### Add or edit a player
Each player is one file in `_players/`. Copy an existing file (e.g.
`_players/hallie-kelly.md`) and rename it to the new player's name
(e.g. `_players/new-player.md`). Edit the fields at the top between the `---`
lines:

```
name: "Player Name"
number: 00
grad_year: 2028
hometown: "City, ST"
high_school: "High School Name"
gpa: "4.00"
position: "Primary Pos/Secondary Pos"
bt: "R/R"
photo:              # leave blank, or set to /assets/images/players/filename.jpg
x_handle: ""        # X (Twitter) username, no @
insta_handle: ""    # Instagram username, no @
```

To add a photo, drop the image file into `assets/images/players/` and set
`photo: "/assets/images/players/filename.jpg"` in that player's file. Square
or portrait (4:5) photos work best.

Optional fields you can add to any player, copying the format from
`_players/claire-carver.md`:
- `study_area`, `high_school_team`
- `measurables:` (a list of label/value pairs — velocity, times, etc.)
- `honors:` (a bullet list of awards)

You can also write freeform text below the second `---` in any player file —
it will appear in an "About" section on that player's page.

### Update team/coach info
Edit the `team:` section at the top of `_config.yml` — coach names, phone
numbers, and social handles all live there and update everywhere on the site
automatically.

### Swap the team photo or logo
Replace `assets/images/team-photo.jpg` or
`assets/images/logos/athletics-logo.jpg` with a new file of the same name
(or update the filename referenced in `index.md` / `_includes/header.html`).

## A note on player privacy

Player profile pages intentionally leave out home addresses, personal phone
numbers, personal emails, and NCAA ID numbers, since this is a public website
that search engines and bots can crawl. If you want to share a full detailed
recruiting packet with a specific college coach, that's best done as a private
PDF or email rather than adding those fields to the public site.
