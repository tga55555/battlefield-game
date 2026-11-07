# Battlefield: Ship Assault

A browser-based top-down multiplayer arcade shooter for 2–4 players on a single ship deck.

## Run it
Open the GitHub Pages site after enabling Pages. One player selects **Create room** and shares the room code. Up to three friends enter that code and select **Join room**.

## Controls
- Desktop: WASD / arrow keys to move, mouse to aim, click to fire, Space to throw a grenade.
- Mobile: direction pad, FIRE and GRENADE buttons.

## Multiplayer
This prototype uses PeerJS/WebRTC data connections with the room creator acting as the game host. It requires an internet connection and uses PeerJS's public signaling service. Peer-to-peer connectivity can vary with network/NAT settings; a production release should use an authoritative game server, input validation, rate limits, and abuse protections.

## Deploy with GitHub Pages
1. Open repository **Settings** → **Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Choose branch **main** and folder **/(root)**, then **Save**.
4. Wait for GitHub Pages to publish. The URL is usually `https://tga55555.github.io/battlefield-game/`.

This prototype does not collect account passwords, API keys, or game credentials.
