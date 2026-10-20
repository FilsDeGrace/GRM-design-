# GameLedger Design System

## Overview
GameLedger is a global **football** app: live head-to-head prediction markets on match stats, plus pre-match tips and a prediction model. Character: calm, precise, premium, trustworthy. Dense but never cluttered. Light theme is the default; dark has full parity. Borrow layout clarity from modern trading and prediction-market apps, but every screen must read as football (fixtures, score, minute, kickoff, window ranges). Never use candlestick charts, order books, Buy/Sell tabs, leverage, price tickers or coin icons.

## Colors
| Role | Light | Dark |
| --- | --- | --- |
| Background | #f3f5f2 | #0c1115 |
| Surface | #ffffff | #121b20 |
| Surface raised | #e8eeea | #1a272e |
| Border / hairline | #ccd6d1 | #2c3b42 |
| Text | #111a1e | #f0f4f2 |
| Text muted | #52626a | #a1afb4 |
| Primary (signal gold) | #805700 | #ffcc66 |
| Intelligence (model) | #4b57a9 | #9aa8ff |
| Live | #076d7a | #69d4e0 |
| Positive | #096b51 | #66d3a9 |
| Negative | #b33c35 | #ff8278 |
| Open | #205d9a | #7cb9ff |
| Locked | #5a6971 | #a1afb4 |
| Pending | #6144b1 | #b7a4ff |
| Void | #8b5a32 | #d9a477 |

Primary gold is for the main action and the selected state only. Status colors are for status only and are always paired with a label or icon. Target WCAG AA contrast in both themes.

## Typography
One neutral grotesque (Inter or similar). Scale: 11 meta, 12 label, 13 body, 15 title, 18 screen heading, 24 hero. Weights 400 and 600 only. Figures use tabular numerals in the same family; monospace only for booking codes and wallet addresses. Uppercase only for status chips. Nothing below 11px.

## Layout and spacing
Design at 390 x 844 (check 360 x 800 and 430 x 932). 8px grid. Screen padding 16. Card padding 14 to 16. Touch targets at least 44px. Header at most 96px: logo, full-width mode switch (Markets | Tips), balance chip and avatar (guests see Sign in). Bottom nav per mode: Markets = Live, Positions, Results; Tips = Tipsters, GRM, Tickets (Studio for creators only).

## Shape and elevation
Radius 12 for cards and sheets, 9 for buttons and inputs, 6 for chips. Hairline borders. Almost no shadows; use elevation only on the selected outcome and on sheets. No boxes nested inside boxes.

## Components
- **Market card:** competition (muted) with status chip and lock countdown on the right; the question (15/600, max 2 lines); two equal outcome pills (team and probability, one selected); a slim split bar with pool total; one row with payout label ("If HFC wins") and a 44px Stake button. Non-open states replace the stake row with one status line.
- **Match-window rail:** a thin timeline of the match with the market window highlighted. It is part of the identity.
- **List row:** identity left (name, quiet subtitle), tabular figures right with a colored delta or status.
- **Tab strip:** underlined active tab. **Filter chips:** filled when active.
- **Stat cards:** three across, label above figure.
- **Status chip:** open, locked, live, pending, settled, void, disputed.
- **Buttons:** primary = gold fill, full width in sheets; secondary = outline. **Inputs:** 44px tall, clear label, visible focus.
- **Bottom sheet:** handle, title, close button, scrollable body, primary button always visible, works with the keyboard open.
- **Ticket card:** legs (fixture, market, selection, odds), total odds, bookmaker, booking code with copy.

- **Post card:** avatar, name, badge, time, body, optional attached ticket with live status chip, action row (like, comment, tip, share). Variants: normal, ticket-settled, Promoted (always labeled), Official, subscribers-only locked.
- **Badges:** Verified Creator (performance-verified), Trial, Official (platform). Distinct shapes and labels, never color alone.
- **Profile header:** banner, avatar, name, badge, bio, counts, analytics strip with sample sizes, tabs General and Subscribers only.
- **Chat bubble:** avatar, name, message, time, slow-mode and system-message variants.
- **Leaderboard row:** rank, avatar, name with badge, ROI with sample size, change arrow, low-sample marker.
- **Tip sheet and Promoted label:** quick amounts and a clear "Promoted" tag.
- **PIN pad:** six masked dots and a numeric keypad with 44px keys, wrong-PIN and locked states.

## Motion
Only for sheet open and close, button press, state changes and countdowns. Short and subtle. Respect reduced motion.

## Do
Show a sample size next to every percentage. Use fictional teams, a TEST token and a "Base Sepolia, Test network" label. Plain language for a stranger. Buttons name the action.

## Don't
No real brands, clubs or people. No region-specific names or currencies. No logos, icons or wording copied from other products. Never expand the letters GRM. No chat UI in this round.
