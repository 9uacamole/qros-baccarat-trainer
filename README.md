QROS Baccarat Trainer v17 — Account UX + Cloud Persistence
============================================================

QROS Baccarat Trainer v17 builds on the v15 mobile-responsive trainer and the v16 account/cloud foundation.

V17 ACCOUNT UX + CLOUD PERSISTENCE
- Added a dedicated QROS Account popup with separate SIGN IN and REGISTER tabs.
- Added clear registration, sign-in, success, warning, and error status messages.
- Added confirm-password validation during registration.
- Added explicit email-verification instructions after account registration.
- Added RESEND VERIFICATION EMAIL support.
- Added clearer handling for incorrect credentials and unverified accounts.
- Added signed-in account identity display.
- Added SAVE TO CLOUD and RESTORE CLOUD controls for authenticated users.
- Local autosave remains active while signed out and continues protecting the trainer session on the same browser/device.
- Account popup is responsive for desktop and mobile use.

V16 SUPABASE ACCOUNT + STORAGE FOUNDATION
- Added the Account control to the trainer interface.
- Added Supabase authentication integration for QROS user accounts.
- Added authenticated cloud persistence using the trainer_state table.
- Added per-user cloud state protection through Supabase Row Level Security policies.
- Added cloud save/restore foundation so a signed-in trainer state can persist independently of local browser storage.
- Existing local trainer persistence remains available alongside cloud persistence.
- Existing baccarat simulation, road logic, bankroll/session behavior, and practice controls are preserved.

V15 MOBILE RESPONSIVE
- Added responsive Android/iPhone layouts for portrait and landscape modes.
- On phones, the Practice Bet panel becomes a compact bottom control dock so it does not cover most of the roads.
- Desktop drag-position behavior remains available on wider screens.
- iPhone safe-area insets and touch scrolling are supported.

QROS Baccarat Trainer v11 — Standard Big Road + Tie Dots


QROS Baccarat Trainer v4 — Non-Commission

Features:
- Real 8-deck (416-card) shuffled shoe simulation
- Baccarat burn + cut-card handling
- Exact baccarat natural and third-card dealing rules
- Visible Player and Banker dealt cards and totals
- Banker 1:1, Player 1:1, Tie 8:1
- Banker/Player bets PUSH on Tie
- Big Road, Bead Plate, Big Eye Boy, Small Road, Cockroach Road
- Tiger-style NEXT RESULT ROAD MAP showing the derived-road mark produced if the next result is Banker or Player
- QROS learning/casino modes and decision-vs-outcome grading
- Demo bankroll and chips only

Run START_TRAINER.bat or open index.html for local use.

ONLINE / GITHUB PAGES
- The trainer can also run from the GitHub Pages deployment.
- Local autosave is browser/device-specific.
- For cross-device/session persistence, sign in to the QROS Account and use cloud persistence.
- A GitHub deployment update is not itself a cloud backup; confirm the account is signed in and the trainer state has been saved/restored successfully.

Important: The next-result road map is a derived-road projection, not a guarantee or prediction of the undealt baccarat result.

V5 DERIVED-ROAD CORRECTION
- Corrected Big Eye Boy, Small Road and Cockroach calculations to use logical Big Road streak columns.
- Dragon tails are treated as infinitely deep for derived-road purposes.
- Corrected the same-row/above comparison: RED when both cells exist OR both are blank; BLUE when exactly one exists.
- Therefore, whenever both hypothetical BANKER and PLAYER next results produce a derived-road mark, the two projected colors for that road are opposites.
- Non-commission demo payout remains Banker 1:1, Player 1:1, Tie 8:1, Banker/Player push on Tie.
- Visible card dealing remains enabled.


QROS Baccarat Trainer v7 layout update
- Practice Bet moved directly below Derived-Road Next-Hand Analysis.
- Demo Chips moved directly below Practice Bet.
- Bead Plate + Big Eye Boy are side by side.
- Small Road + Cockroach Road are side by side below them.
- Big Road and Bead Plate grids now render grid lines across the full visible board.
- Every road automatically scrolls to the newest/rightmost road cells when horizontal overflow begins.
- Corrected derived-road logic and non-commission card-dealing game behavior are preserved.


v7 changes:
- Big Eye Boy board has one additional visible grid row.
- Place Practice Bet card can be dragged anywhere on screen; position persists locally. Double-click its header to reset it to the sidebar.
- Road auto-scroll and full-width grid behavior from v6 preserved.

v8 B6/S6 Big Road update:
- Banker win with total 6 using 3 Banker cards shows B6 at the top-right of that Banker Big Road stamp.
- Banker win with total 6 using 2 Banker cards shows S6 at the top-right of that Banker Big Road stamp.
- Non-commission payouts, corrected derived roads, draggable practice bet, full grids, and road auto-scroll are preserved.


v10 Standard Big Road collision update:
- Corrected Big Road display behavior to baccarat-standard sticky horizontal continuation.
- When a streak is blocked by an occupied cell below or reaches the sixth row, it turns right.
- Once that streak turns right, all later results in the same Banker/Player streak continue horizontally until the side changes; it does not drop down again when a free lower cell appears.
- Applied the same display-placement rule to Big Eye Boy, Small Road, and Cockroach Road chart layouts.
- Corrected logical derived-road calculations remain unchanged.
- Equal 6-row/30px grid sizing for Bead Plate and all three derived-road panels is preserved.


v11 Big Road Tie indicator update:
- A Tie does not create a new Big Road cell.
- Each Tie is shown as a small green dot attached to the previous Banker/Player Big Road stamp.
- Two consecutive Ties produce two green dots; additional consecutive Ties continue adding dots.
- Leading Tie(s) are attached to the first Banker/Player result when it appears.
- B6/S6 badge remains at the Banker stamp top-right; Tie dots use the top-left to avoid overlap.

V12 update:
- Horizontal road scrollbars are permanently allocated/visible instead of appearing only after overflow, preventing road cards from jumping when the scrollbar first appears.

V13 last-hand / shoe transition update:
- The cut-card threshold is detected during the hand; that hand is allowed to finish normally.
- When the cut card is reached, the completed hand is clearly marked as the LAST HAND OF THIS SHOE.
- The final Player/Banker cards, totals, result, Big Road, and derived roads remain visible for review.
- The Deal button changes to START NEW SHOE instead of automatically replacing the final result.
- Press START NEW SHOE when ready; only then are the roads reset and the next shuffled shoe prepared, while session bankroll/P&L continue.
