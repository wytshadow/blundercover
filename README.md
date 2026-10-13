# BlunderCover — iOS prototype

BlunderCover is an in-development native iOS chess study and post-game coaching app. This repository is a public project showcase, not the application's source-code distribution or a downloadable release.

![BlunderCover logo](assets/logo-200.png)

## Watch the prototype

Press **Play** below to watch directly in your browser—no download or YouTube account needed.

https://github.com/user-attachments/assets/68eb89af-9a48-4412-9dd0-435c52275547

This ~43-second recording shows the actual current iOS simulator app: Home, legal board entry, Library and More navigation, genuine on-device Stockfish review results, and practice from a reviewed mistake. It uses synthetic demo players **chessuser1**, **chessuser2** and **chessuser3**, not real account data. Idle startup/relaunch screens were trimmed, and navigation is presented before review/practice. No mock UI or private account data is shown.

[Open the browser-playable demo separately](https://github.com/wytshadow/blundercover/issues/1) if your viewer does not display GitHub's embedded player.

The two native UI flows used to record this refreshed demo passed on October 12, 2026. This video demonstrates a working prototype, not full feature acceptance or approved Chess.com Game Review access.

## Working prototype

- Import and replay completed games, preserving PGN comments and variations.
- Link player identities and import public Chess.com and Lichess histories.
- Display Chess.com's published accuracy scores and existing Lichess PGN evaluation annotations separately from on-device Stockfish reviews.
- Practice opening repertoires, authored puzzles and positions drawn from post-game reviews.
- Connect to Lichess using Authorization Code + PKCE with read-only study and puzzle scopes.
- Export and restore encrypted, portable backups without including account credentials.

The interface includes Home, Practice, OTB Entry, Library and More. The prototype is implemented in SwiftUI and has been exercised through native simulator UI tests, real provider-history imports, on-device Stockfish review and encrypted backup roundtrips. Physical-device acceptance and distribution validation remain pending.

## Requested Chess.com access

We are applying for OAuth account linking and supported read-only access to a user's completed games and existing analysis. Full authenticated Game Review retrieval is not implemented or claimed; approval and documentation of an appropriate analysis-access API are needed. Published public accuracy scores are not a substitute for full move-by-move Game Review.

BlunderCover does not submit moves, automate play, provide live-game assistance or connect a physical chessboard. Connected Board access is not requested.

## Data boundaries

This showcase contains no user games, private notes, account credentials, simulator data or test logs. The prototype stores its study library locally and its Lichess access credential in the device Keychain. Provider requests are sent to the selected provider; portable backup files are saved to the user's chosen destination. This summary is not a published legal privacy policy or terms of service.

BlunderCover is an independent project, not endorsed by Chess.com or Lichess. No public app release is offered here.
