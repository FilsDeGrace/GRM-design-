# Screen prompts for UX Pilot (v2, S1 to S29)

Paste the **Global Context** first in every new session. Then paste one screen prompt at a time. Generate S1 first and get it approved before the rest.

## Global Context
```
Design a mobile-first (390x844) app called GameLedger, a global football app with two modes: Markets, named IN-90 Football (live prediction markets on match stats, staked in a TEST token on a test network), and Tips (an X-like social platform for pre-match tipsters, news and banter, plus a prediction model called GRM). This is a football app, not a crypto exchange: every screen must read as football at a glance (fixtures, live score and match minute, kickoff times, fictional team badges, window ranges like 65'-80', corner and card counts) and must not show candlestick charts, order books, Buy/Sell tabs, leverage or price tickers. Look and feel: the calm, dense, premium clarity of a modern trading app, applied to football content, with our own identity. A thin match-window rail (a timeline of the match with the market window highlighted) is part of the identity on market cards. Use the attached tokens (warm gold accent, light theme default, dark parity), Inter-style type on this scale: 11, 12, 13, 15, 18, 24, weights 400 and 600, tabular figures. Calm density, hairline dividers, few boxes, 44px touch targets, radius 12, 8px grid. Take patterns (not logos, icons, wording or colors) from the reference screenshots. Header: logo, a full-width mode switch (Markets | Tips), balance chip and avatar (guests see Sign in). Bottom nav per mode: Markets = Live, Positions, Results; Tips = Tipsters, GRM, Tickets. Fictional teams only, no real brands, no region-specific names. Show a sample size next to every percentage. Never expand the letters GRM.
```

## S1. Markets: Live list (HERO SCREEN, do this first)
```
Markets mode, Live tab, signed-in user. Header with mode switch (Markets selected), balance chip "1,000 TEST" and avatar. Under it a scrollable category strip (All, Corners, Cards, Shots, Fouls) and an underlined tab row (Live first, Upcoming, All). Then a featured hero carousel with page dots (one featured market), then a vertical list of 5 compact market cards from different fictional fixtures. Each card: competition (muted) and status chip with lock countdown on the right; the question (max 2 lines); two equal outcome pills with team and probability (one selected); a slim split bar with pool total; one row with "If HFC wins" payout and a 44px "Stake 50" button. Locked, live and pending cards replace the stake row with one status line. Bottom nav: Live, Positions, Results.
```

## S2. Stake ticket (bottom sheet)
```
Stake ticket as a bottom sheet over the Live list. Title: the market question. A split probability bar with both sides. Amount field with steps 25, 50, 75, 100% of balance. Lines: Available, Rake 5%, Est payout if HFC wins. One full-width primary button "Confirm stake 50 TEST". Show four variants: default, keyboard open (field and button visible above the keyboard), pending ("Confirming..."), and error (insufficient balance).
```

## S3. Market card states
```
A sheet of the compact market card in every state: open, locked (review in progress), live (window 65-80'), pending (stability countdown), settled-won, settled-lost, void (postponed), void (feed outage), disputed. Same layout, only the status line and chip change. Include light and dark.
```

## S4. Sign-in flow
```
Guest taps Stake and a sign-in bottom sheet appears: email field, Continue with email, Google, Apple, divider, "Connect a wallet you already have", one reassurance line about no spending without confirmation. Then: 6-digit code entry with resend, a username step with live availability (checking, available, taken), a welcome sheet with the test-funds faucet, and a final "Confirm stake" step. Also a "Session expired, sign in again" sheet that keeps the user's place. Make sure the whole sheet, including the primary button, is visible with the keyboard open.
```

## S5. Positions and Results
```
Markets mode. Positions tab: stat cards (Open, Claimable, Total staked) then list rows of open positions with market, side, stake, status and a Claim button when claimable; an empty state. Results tab: filter chips (Settled, Void, Disputed) and list rows. Then a settlement receipt screen: final counts per team, a feed-event timeline, result hash, payout or refund, a Claim or Refund button, and a "Dispute" link inside the dispute window.
```

## S6. Tips: Tipsters list
```
Tips mode, Tipsters tab. Mode switch with Tips selected. Underlined tabs (Top, New, Following). Filter chips (ROI, Avg odds, Sample size, Price). Three-up stat cards. List rows: avatar, handle, a verified or trial badge, ROI with sample size, average odds, streak, monthly price, and a Follow button. Low sample sizes show a visible low-confidence marker.
```

## S7. Creator page and pick card
```
A tipster's page: header with avatar, handle, badge, Follow and Subscribe buttons. Stat cards (ROI, units, avg odds, sample size, streak). An odds-range bar. A list of pre-match picks as tickets: legs (fixture, market, selection, odds), total odds, bookmaker, booking code with copy button, short analysis, kickoff time, status (pending, won, lost, partial, void). Include one deleted-pick tombstone. Locked picks for non-subscribers. A Convert-code action for subscribers.
```

## S8. Subscribe sheet
```
Subscribe bottom sheet for a tipster: weekly and monthly plans (paid upfront, no auto-renew), price in TEST, wallet confirmation step, then pending, active (with expiry date), failed, and expired states.
```

## S9. GRM tab
```
Tips mode, GRM tab. A header card with track record and sample size. Free and Pro tier panel. Top parlays: each a ticket card with legs, total odds, confidence and sample size, and an expandable per-leg analysis row (model estimate, confidence, n). Below, individual pick cards. Each ticket has "Edit ticket" (remove or restore legs, at least 2 legs, odds recalculate) and "Book this ticket". A clear "Open in GRM Pro" link row explains that the full match list and detailed editing are in a separate web app. No booking-code input anywhere.
```

## S10. Book this ticket
```
Bottom sheet: choose a bookmaker (three neutral options). Then three results: success (booking code with copy and an "Open bookmaker" link; nothing is placed automatically), partial (list of unmapped legs with Remove and retry), failure (reason and retry). Include a loading state.
```

## S11. Tickets tab
```
Tips mode, Tickets tab. Sections: Booked GRM tickets (code, bookmaker, link), Saved tickets, Copied tipster picks with result status. Empty state for each.
```

## S12. Me and wallet sheet
```
Me page opened from the avatar: username, wallet address (shortened, copy), session status and expiry, subscriptions, notification toggles, theme (Light, Dark), network label (Base Sepolia, Test network), Sign out. Also the wallet bottom sheet from the balance chip: balance, address, faucet button with remaining daily allowance.
```

## S13. Studio (creators)
```
Studio for an approved creator, shown as a fourth Tips tab: trial progress ring with day count and pick count, a pick composer (legs, odds, bookmaker, booking code, analysis, server-time notice, odds cap of 30), my picks, and earnings with a holdback note and Claim button. Also an eligibility result screen (passed, and failed with reasons) and a suspended notice.
```

## S14. System states
```
A sheet of reusable states in light and dark: skeleton list, empty, error with retry, offline with last-updated time, toast (success and error), and a pending-transaction indicator in the header that persists across a mode switch.
```

## S15. Mode switching variants
```
Show both ways to switch between Markets and Tips on the Live and Tipsters screens: Variant A, a full-width segmented switch in the header; Variant B, a raised center button in the bottom bar that swaps modes while the sides hold the current mode's tabs. Recommend one and say why.
```

## S16. Ops console (desktop 1440x900)
```
Desktop admin console with a left rail (Markets, Templates, Feeds, Disputes, Creators, Audit log). Market list with state filter chips and a table: market, fixture, state, pool, lock time, feed status, actions. A market detail view with state timeline, pool split, feed events, void and settle actions that require a reason, and an audit trail. Dense, calm, same tokens.
```

## S17. Tips Home feed (X-like)
```
Tips mode, Home tab. Header with mode switch (Tips selected), balance chip and avatar. Underlined tabs: General, News, Community tips, with a swipe hint to a Subscribers-only feed. Sport filter chips (All, Football, Basketball, NFL, Tennis). A feed of post cards: avatar, name, badge (Verified Creator, Trial or Official), time, text, optional attached ticket (legs, total odds, live status chip), and an action row (like, comment, tip, share). Show variants: a normal post, a post with a ticket that has settled as won, a Promoted post (clearly labeled), an automated Official GRM post (digest of top-league fixtures with an attached ticket), and a Subscribers-only post locked for a non-subscriber. Raised "+" compose button in the bottom bar. Bottom nav: Home, Creators, GRM, Tickets.
```

## S18. Post composer
```
Full-screen composer. Text field with character count. Audience toggle: General or Subscribers only (subscribers option only for creators). Attach a pre-match ticket (pick legs, then it shows odds; note that it locks at kickoff and cannot be edited). Tags for sport and league. A one-line notice: "Tips are opinions, not guarantees." Show states: empty, filled, blocked by the rules (banned word, too many links, guaranteed-win claim) with a clear inline message, and posting.
```

## S19. Creator profile (X-like)
```
A creator profile: banner, avatar, name, Verified Creator badge, bio, counts (followers, following, subscribers). Analytics strip: ROI, hit rate, sample size, average odds, streak, specialties, each with its sample size. Buttons: Follow, Subscribe, Tip. Tabs: General, Subscribers only, Picks, About. Subscribers-only tab shows locked previews to non-subscribers. Show light and dark, and the Official GRM profile variant (automated, with a link to open GRM Pro).
```

## S20. Post detail and comments
```
A single post with its comments thread. Reactions (like and a laugh reaction), a tip button, a report menu. Show moderation states: comment hidden by the author, comment removed by moderators with a reason, and a rate-limit notice when commenting too fast.
```

## S21. Tip sheet with PIN
```
A bottom sheet to tip a creator or a post author: quick amounts (1, 5, 10 TEST), custom amount with no limit, optional short message, a confirm button. After confirm, a PIN entry step (6-digit keypad, dots, "Forgot PIN"). Then pending, success and failed states. Show the wrong-PIN state ("Wrong PIN, 3 tries left") and the locked state ("Too many tries, try again in 15 minutes"). Also the "Tip received" notification row.
```

## S22. Leaderboards
```
A leaderboards screen with tabs: Top earners (IN-90 Football), Overall (live), Top creators, Top community tipsters. Window chips: Week, Month, All-time. Sport chips. Rows: rank, avatar, name with badge, ROI with sample size, change arrow, and a low-sample marker. A pinned "Your rank" card at the bottom with a Hide me option. A minimum-sample note explains why some users are unranked.
```

## S23. IN-90 Room (Markets mode)
```
Markets mode, Room tab. Match context header (teams, score, minute) and a pinned rules strip. Tabs: Chat and Thesis. Chat: message bubbles with avatars, a slow-mode indicator, a "Chat is not advice" reminder, a system message "Market locked, chat is quiet for 30 seconds", mute and report on long-press, and an inline error when a message contains blocked language or begging. Thesis tab: short thesis posts with an optional "I staked 50 on HFC" proof chip, likes and comments. Bottom nav: Live, Positions, Leaders, Room.
```

## S24. Reach (promote a post)
```
Creator tool to promote a post: choose a post, choose a target (a match or a date), budget in TEST, duration, estimated reach, and a preview of the Promoted label in the feed. A rules checklist (record requirement, no guaranteed-win claims). Then a campaigns list with status (in review, live, ended) and stats (views, follows, subscribers gained).
```

## S25. Notifications inbox
```
Notifications list with filter chips (All, Markets, Social, Money). Items: market settled, claim available, new reply, new follower, new subscriber, tip received, subscription expiring, promotion approved, report outcome. Read and unread states, plus an empty state.
```

## S26. Sport selector
```
Show how the sport switches in both modes: in Markets mode the header shows "IN-90 Football" with a sport switcher (other sports shown as coming soon, names not decided); in Tips mode a row of sport filter chips on Home and Creators. Include an onboarding step where a new user picks sports and leagues.
```

## S27. Safety and moderation UI
```
User-facing safety screens: a report sheet (reason list, optional note), block and mute confirmation, community rules sheet, new-account limit notice (for example, links are restricted for 7 days), an 18+ confirmation step, and responsible-play settings (daily stake limit, cool-off, self-exclusion) with a reality-check prompt after a long session.
```

## S28. Ops: moderation and ads (desktop 1440x900)
```
Desktop admin screens in the same style: a moderation queue (reports with post preview, author history, actions: remove, warn, mute, ban, with reason and an audit entry), an ads review queue (promoted posts awaiting approval with the rules checklist), and a creator verification review. Dense, calm.
```

## S29. Transaction PIN
```
PIN screens: set a 6-digit PIN (enter, confirm, mismatch error, a note that the PIN protects tips if someone gets into the account), a PIN entry sheet used before a tip, wrong-PIN and locked states, and a reset flow (email code, then wallet signature, then new PIN). Also a Me > Security row to change or reset the PIN. A numeric keypad with large 44px keys, masked dots, and no PIN shown on screen.
```
