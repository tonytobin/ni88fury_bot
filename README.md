# ni88fury_bot

A macOS-friendly YouTube Live companion for chat automation, audio alerts, viewer welcomes, and OBS overlays, simulate key-press, interactive Mini Games for viewers.

ni88fury_bot helps streamers turn live chat into a more interactive part of the broadcast. It connects to YouTube Live, responds to viewers, allows viewers to play mini games, plays sounds, triggers media, and displays custom browser-source experiences in OBS and simulate custom keypress. The app is totally free to use.

## screenshots

<img width="2290" height="1572" alt="Screenshot 2026-09-14 at 4 07 10 PM" src="https://github.com/user-attachments/assets/9b41fb53-fd1e-42bd-b488-fb49e92c9fad" />

<img width="1060" height="688" alt="Screenshot 2026-08-25 at 5 05 35 PM" src="https://github.com/user-attachments/assets/8ba1bcc8-002e-47e3-9917-ca6b86ad2270" />

<img width="2306" height="1624" alt="Screenshot 2026-09-14 at 3 55 45 PM" src="https://github.com/user-attachments/assets/1a7d3519-2506-4475-9b0d-71379fd28215" />

<img width="2298" height="1618" alt="Screenshot 2026-09-14 at 3 56 01 PM" src="https://github.com/user-attachments/assets/9827e2d3-a4f9-43ba-aae0-cb9e641b29b3" />

<img width="2606" height="1502" alt="Screenshot 2026-09-14 at 3 58 32 PM" src="https://github.com/user-attachments/assets/d555f99d-4f2d-4e52-a43a-4ef1b08c293c" />

<img width="776" height="764" alt="Screenshot 2026-09-14 at 3 59 22 PM" src="https://github.com/user-attachments/assets/7909c43c-e4c3-439b-9c13-c5b8ebe467e6" />

<img width="794" height="734" alt="Screenshot 2026-09-14 at 3 59 38 PM" src="https://github.com/user-attachments/assets/e0127125-801c-4495-aa2b-54346ea47423" />

<img width="2286" height="1616" alt="Screenshot 2026-09-14 at 4 00 22 PM" src="https://github.com/user-attachments/assets/83069f1e-eef4-4104-a14b-8aeb0a918086" />




# imp
The bot replies you see in the screenshots are based on the "bot name" you give in the app settings. The bot will be posting under your youtube channel name during a real live stream and not as "ni88fury bot". For example if your channel name is "abc", the bot replies will be done under the name "abc".

## Features

- Official YouTube Live chat integration with OAuth.
- Development mode with simulated livestreams and chat messages.
- UI-managed custom commands and natural-language triggers.
- Ordered command actions including:
  - Chat replies.
  - Audio clips.
  - Images and videos.
  - Delays.
  - Keyboard actions.
  - Welcome effects.
  - Custom OBS overlays.
- First-time viewer welcoming.
- Live Mini Games for viewers
- Known-viewer recognition and personalized welcome sequences.
- Configurable chat notification, welcome, and media audio routes.
- Promotional messages with cooldown and activity controls.
- Win, loss, and win-streak tracking.
- Transparent OBS browser sources for:
  - Subscriber count.
  - Temporary media.
  - Welcome effects.
  - Win streaks.
  - Rolling end credits.
  - Custom overlays.
- Movie-style end credits showing unique viewers from the livestream.
- Viewer participation highlights based on message count.
- Support for custom image, GIF, video, and HTML overlays.

Everything is managed through the in-app configuration.

## Getting Started

### Standalone macOS App

Download the latest release from the Releases page.

1. Extract the downloaded zip file.
2. Move `Ni88Fury Bot.app` to your Applications folder.
3. Open the app.
4. If macOS shows a security warning, use **Right-click > Open** the first time.
5. Start in development mode to explore the app with simulated streams.
6. Switch to production mode when you are ready to connect to YouTube.

The current packaged release targets Apple Silicon Macs. Intel builds can be provided separately.

### YouTube Setup

Production mode requires YouTube OAuth authorization.

From the welcome screen:

1. Switch from development mode to production mode.
2. Select your Google Desktop OAuth credentials file.
3. Press the OAuth button.
4. Complete the Google authorization flow in your browser.
5. Select one of your active livestreams.

Your OAuth token is stored locally on your computer will never be shared with me or anyone.

## OBS Overlays

The app runs a local browser-source server for OBS.

Example overlay URLs:

```
http://127.0.0.1:8765/overlay.html?mode=subscribers                                                             
http://127.0.0.1:8765/overlay.html?mode=media                                                                         
http://127.0.0.1:8765/overlay.html?mode=win-streak                                                               
http://127.0.0.1:8765/overlay.html?mode=welcome                                                             
http://127.0.0.1:8765/overlay.html?mode=end-credits                                                             
http://127.0.0.1:8765/overlay.html?mode=shoutout                                                                 
http://127.0.0.1:8765/overlay.html?mode=games                                                                         
http://127.0.0.1:8765/overlay.html?mode=deck  
```
Add each URL as an OBS Browser Source. The app displays the available overlay URLs in the interface.

Custom overlays can be created from the in-app overlay settings. Supported custom sources include:

Static images.
Animated GIFs.
Videos.
HTML pages with their own CSS and JavaScript.
Custom overlays can also be triggered from command, welcome, and known-viewer action sequences.

End Credits
At the end of a livestream, press Play end credits from the stream screen.

The bot will:

Send a configurable thank-you message to chat.
Freeze the list of unique viewers from the session.
Display their names in a transparent rolling credits overlay.
Highlight viewers based on their message count.
The end-credit text, viewer filters, highlight thresholds, visual style, message-count visibility, and scroll speed are all configurable through the application.

# Privacy
YouTube communication happens only when production mode is enabled.
OAuth tokens are stored locally.
The OBS server binds to 127.0.0.1 by default.
The app does not require an external dashboard or hosted service.
Local logs may contain chat usernames, viewer IDs, and message text.
Do not share your personal application data folder or OAuth token.

# Project Status
ni88fury_bot is an actively developed project focused on making YouTube livestreams more personal, interactive, and visually engaging.

The current release is macOS-first. I will make windows and linux ports as time permits or based on demand.
