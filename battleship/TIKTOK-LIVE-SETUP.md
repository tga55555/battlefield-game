# SEA HUNT on TikTok LIVE (PC)

## What this adds
The `live.html` page is a transparent browser overlay. It joins the regular SEA HUNT room as one shared player called **TikTok Crew**. TikFinity Desktop forwards LIVE chat events to the overlay over its local Event API.

Viewers type `!fire B7` (A1–J10) in TikTok chat. A valid command fires for the shared TikTok Crew player only when it is that player's turn. The first valid shot wins the turn; repeated commands and already-fired coordinates are ignored by the game. `!help` displays the command reminder in the overlay.

## Setup

1. Open SEA HUNT on the streaming PC: https://tga55555.github.io/battlefield-game/battleship/
2. Create a game. The host page shows a six-character room code.
3. Install/open TikFinity Desktop and connect it to the same TikTok account that is going LIVE. Keep TikFinity Desktop running during the stream. Its Event API listens at `ws://localhost:21213/`.
4. In TikTok LIVE Studio, add a **Link** or **Browser** source.
5. Use this URL, replacing `ROOMCODE` with the room code from step 2:
   `https://tga55555.github.io/battlefield-game/battleship/live.html?room=ROOMCODE`
6. Size the source for your scene (try 560 × 850), position it where viewers can see it, and keep its background transparent.
7. Return to the SEA HUNT host page. The overlay joins as **TikTok Crew**. Start the battle once at least two players are connected.
8. Test with a chat message such as `!fire B7` when TikTok Crew's turn appears. The overlay also has a local test field for checking its turn/command display.

## Notes

- TikFinity Desktop and TikTok LIVE Studio must run on the same PC because the overlay reads TikFinity's local WebSocket.
- The browser overlay is a separate SEA HUNT player; it does not take over the host's controls. The host can still play from the normal game page.
- With two players, the match is the streamer versus the whole TikTok chat as one shared captain. More players can join the normal room up to the game's four-player limit.
- Chat commands are only accepted on the TikTok Crew turn. Ask viewers to wait for the overlay to say it is their turn.
- This integration uses TikFinity's local Event API. TikTok's own chat connection and third-party tool availability can change; test before going LIVE.
