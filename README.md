# BlunderCover — iOS prototype

BlunderCover is an in-development native iOS chess study and post-game coaching app that brings **over-the-board (OTB), Chess.com and Lichess games into one personal coaching library**. Enter OTB games on a legal chessboard, import your online games, review decisions with Stockfish, and compare recurring positions across both to understand patterns in your play and build targeted mistake practice. This repository is a public project showcase, not the application's source-code distribution or a downloadable release.

![BlunderCover logo](assets/logo-200.png)

## Watch the prototype

Press **Play** below to watch directly in your browser—no download or YouTube account needed.

https://github.com/user-attachments/assets/8d0dddc2-ecd6-4731-930a-f39557d9f652

This **64-second recording of the actual iOS app** uses the owner's authorized USCF identity (**30413872**), Chess.com and Lichess accounts (**wytshadow** on both), and selected saved games. The separate demo library contains 11 real Chess.com games and 5 real Lichess games, plus an instructional OTB game entered during the recording.

The demo shows:

1. Home populated with actual USCF, Chess.com and Lichess ratings and recent games.
2. Full legal-board entry of **Scholar's Mate**: `1. e4 e5 2. Qh5 Nc6 3. Bc4 Nf6 4. Qxf7#`.
3. Saving that OTB demonstration with players/event/result, and replaying it from the shared Library alongside online games.
4. A fresh on-device Stockfish review of the OTB game, followed by a saved Stockfish review of a real Chess.com game. Published Chess.com accuracy remains separately labeled.
5. Practice from a real reviewed mistake, then recurring-position evidence that includes both the OTB demonstration and real online games.

Scholar's Mate is explicitly labeled **OTB demonstration**, not a claimed real tournament result; `chessuser1` is its synthetic opponent. The online games and ratings are real. Startup screens and idle automation navigation were trimmed; the app UI and results are not mocked. Both recorded native UI flows passed on October 12, 2026.

[Open the browser-playable demo separately](https://github.com/wytshadow/blundercover/issues/1) if your viewer does not display GitHub's embedded player. This is a working prototype demonstration, not full feature acceptance or approved Chess.com Game Review access.

## Working prototype

- **Enter OTB games move by move** on a legal chessboard, including captures, promotions, undo/redo, comments and variations; save the completed game to Library with players, event and result.
- **Combine OTB and online games** under a confirmed player profile. Import completed human Rapid games from Chess.com and Lichess, preserving PGN comments and variations.
- **Compare recurring positions across your games**: see repeated choices, game samples and outcomes, then inspect the underlying games and compare repertoire, human and engine evidence. These summaries describe repeated positions and whole-game results; they do not label a move a mistake merely because its game was lost.
- **Review decisions with on-device Stockfish** and practice sufficiently supported mistakes from your OTB or online games. Review evidence includes measured depth, nodes and search time.
- **Keep provider analysis distinct**: display Chess.com's published accuracy scores and existing Lichess PGN evaluation annotations separately from local Stockfish reviews. Full authenticated Chess.com Game Review access is still being requested.
- **See current ratings** from USCF, Chess.com and Lichess on Home, with source/freshness information, alongside recent games and upcoming events.
- Practice opening repertoires, authored puzzles and positions drawn from post-game reviews.
- Connect to Lichess using Authorization Code + PKCE with read-only study and puzzle scopes.
- Export and restore encrypted, portable backups without including account credentials.

### Why combine OTB and online games?

A player's opening habits and missed opportunities can recur across both environments. Keeping the games linked to the same identity lets the player compare those situations and use actual Stockfish reviews to turn supported mistakes into training. The current prototype includes shared coaching-game lists, cross-game recurring-position summaries and per-game engine reviews; it is not claiming a completed automatic mistake-category classifier.

The interface includes Home, Practice, OTB Entry, Library and More. The prototype is implemented in SwiftUI and has been exercised through native simulator UI tests, real provider-history imports, on-device Stockfish review and encrypted backup roundtrips. Physical-device acceptance and distribution validation remain pending.

## Requested Chess.com access

We are applying for OAuth account linking and supported read-only access to a user's completed games and existing analysis. Full authenticated Game Review retrieval is not implemented or claimed; approval and documentation of an appropriate analysis-access API are needed. Published public accuracy scores are not a substitute for full move-by-move Game Review.

BlunderCover does not submit moves, automate play, provide live-game assistance or connect a physical chessboard. Connected Board access is not requested.

## Data boundaries

The demo includes the project owner’s explicitly authorized public identity, USCF ID, ratings and selected saved games. Scholar’s Mate is an instructional OTB demonstration, not a claimed real tournament game. No credentials, private notes, downloadable library/database archives or test logs are published. The prototype stores its study library locally and its Lichess access credential in the device Keychain. Provider requests are sent to the selected provider; portable backup files are saved to the user's chosen destination. This summary is not a published legal privacy policy or terms of service.

BlunderCover is an independent project, not endorsed by Chess.com or Lichess. No public app release is offered here.
