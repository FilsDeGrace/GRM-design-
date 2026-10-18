# GameLedger: Design Brief for UX Pilot

## 0. What this is, and what it is not
**This is a football app.** Its content is matches, scores, minutes, kickoff times, teams, tipsters, tickets and a prediction model. It is not a crypto exchange or a trading terminal.
- Borrow only the **layout and clarity patterns** of trading and prediction-market apps. The subject matter must read as football at a glance: fixtures, live score and match minute, team badges (generic fictional placeholders), kickoff times, window ranges like 65'-80', corner and card counts.
- **Do not include:** candlestick or price charts, order books, Buy/Sell tabs, leverage, price tickers, coin icons, or any exchange language. The OKX reference contains some of these; ignore them and use only what the references README lists.
- A subtle football cue belongs in the identity, for example the match-window rail (a thin timeline of the match with the market window highlighted) used on market cards.

## 1. Product
GameLedger is a global, onchain football app with two modes in one mobile-first PWA:
- **Markets mode:** live head-to-head prediction markets on match stats (for example, which team wins more corners between minute 65 and 80). Users stake test tokens into two-sided pools. Markets lock, run, settle from data, and can be voided.
- **Tips mode:** pre-match football tips. Verified tipsters post tickets (legs, odds, bookmaker, booking code, analysis) with a data-settled public record. A GRM section shows a prediction model's pre-match top parlays and single picks. Users can edit a GRM ticket lightly and book it through a bookmaker to get a booking code and link.
- An **Ops console** (desktop) manages markets, feeds, disputes, creators and the audit log.

Audience: global, mobile-first people who already use trading, betting or prediction apps. They want speed, clarity and trust. Fictional teams only. No region-specific names, currencies or brands. Amounts are a test stablecoin labeled TEST on a test network (Base Sepolia).

## 2. Design direction
Goal: the clarity and premium calm of a modern trading app, applied to football content, in our own identity.
Borrow **patterns** from the reference screenshots:
- Calm density: tight type scale, strong hierarchy, hairline dividers, few boxes, no boxes nested in boxes.
- Data rows: identity on the left (name and a quiet subtitle), right-aligned tabular figures with a colored delta or status.
- Underlined tab strips, and filter chips that fill when active.
- Three-up stat cards for summaries.
- Prediction-market card: the question, two outcome pills with probability, a footer with pool or volume, a status chip and a time.
- **Order-ticket pattern for staking:** split probability bar, amount with 25/50/75/100% steps of balance, "Available" and "Est payout" lines, one full-width primary button.
- Hero carousel of featured markets with page dots. A scrollable category strip. A Live count badge.
- Bottom navigation of 3 to 4 items with a clear active state.

Do **not** copy: logos, product names, icons, illustrations, wording, exact colors, proprietary fonts, or pixel layouts. The result must look like GameLedger, not like any other product.

## 3. Theme (keep)
Use `03_TOKENS.json`. Light is the default; dark must have full parity. Accent (`signal`, a warm gold) is for primary actions and the selected state. Semantic colors are for status only. Never rely on color alone; pair status colors with a label or icon. Target WCAG AA contrast in both themes.

## 4. Typography
One neutral grotesque (Inter or similar). A single scale: 11 meta, 12 label, 13 body, 15 title, 18 screen heading, 24 hero. Weights 400 and 600 only. Figures use tabular numerals in the same family; monospace is only for booking codes and wallet addresses. Uppercase only for status chips. No text below 11px.

## 5. Layout and navigation
- Design at 390 x 844; verify 360 x 800 and 430 x 932. Screen padding 16. Card padding 14 to 16. Radius 12. Touch targets at least 44px.
- **Header (both modes):** logo, a full-width **mode switch** (Markets | Tips), then for signed-in users a balance chip (opens a wallet sheet) and an avatar (opens Me). Guests see a Sign in button instead. Keep the header at or under 96px total.
- **Markets bottom nav:** Live, Positions, Results. **Tips bottom nav:** Tipsters, GRM, Tickets, plus Studio for approved creators only.
- Explore **two variants** of mode switching and show both: (A) the header switch above (approved baseline); (B) a raised center button in the bottom bar that swaps modes. Recommend one with a reason.
- Community chat is not designed in this round. Show no chat UI.

## 6. Core components
Mode switch; balance chip; avatar; tab strip; filter chips; stat cards; market card (all states); outcome pill; split probability bar; stake ticket; bottom sheet (with keyboard open); status chip; countdown; list row; pick or ticket card with legs; per-leg analysis row; booking result panel (success, partial, failure); settlement receipt with timeline and result hash; empty, loading, error and offline panels; toast; session-expired sheet.

## 7. States to show
Market: open, locked, live, pending, settled (won and lost), void (postponed, feed outage), disputed. Account: guest, signed in, session expired. System: loading skeletons, empty, error, offline with last-updated time. Money: pending, confirmed, rejected, insufficient balance, market locked during confirmation.

## 8. Content rules
Plain language for a stranger. Buttons name the action ("Stake 50", "Book this ticket"). No development notes. Never expand the letters GRM. Show a sample size next to every percentage. Fictional fixtures only, with varied markets (corners, cards, shots on target, fouls) so the list never repeats the same question.

## 9. Accessibility and motion
44px targets, visible focus, labels for icons, respect reduced motion. Motion only for sheet open and close, button press, state changes and countdowns.
