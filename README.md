# actpat

Statistics and follower graph for ActivityPub accounts.

## Usage

Open `index.html` in any modern browser — no server or build step needed.

Enter an ActivityPub handle in the format `@username@instance.social` and click **Explore**.

## Features

- **Account stats**: followers, following, posts, follower ratio, account age, posting frequency, peak activity day/hour, languages, and estimated reach
- **Follower graph**: interactive force-directed graph of the account's followers and their followers (2 hops, up to 200 accounts)
- **Community detection**: automatic cluster detection using label propagation, with color-coded communities and a filterable legend
- **Graph controls**: zoom, pan, drag nodes, pause/resume simulation, toggle labels
- **Compatible with**: Mastodon, Pleroma, Akkoma, and other Mastodon-API-compatible ActivityPub instances

## Notes

- All data is fetched directly from public ActivityPub instance APIs — no server, no tracking
- Private accounts will appear as isolated nodes (their followers list is not public)
- Some instances may block cross-origin requests (CORS); those nodes are marked with a red badge and their followers are skipped
- Fetching is rate-limited to avoid hammering instances (3 concurrent requests, 400ms delay between batches)
