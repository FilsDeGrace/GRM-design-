# GameLedger: UX Pilot pack

Use this pack to have UX Pilot design the mobile app and the Ops console. GameLedger is a football app; the references are trading and prediction apps used only for layout and clarity patterns. Read in this order:

1. `01_DESIGN_BRIEF.md`: product, design direction, theme, type, rules. Upload it as the project document if your plan supports document-to-design, otherwise paste it as the first prompt.
2. `03_TOKENS.json`: the current theme (colors, radii, type). Import as a design system if your plan allows, otherwise paste the values.
3. `references/`: screenshots. `README` inside explains what to borrow from each. Upload the OKX and Kalshi images as reference images, and the `current-build-*` images only as "what to improve".
4. `02_SCREEN_PROMPTS.md`: one prompt per screen. Paste the Global Context prompt first, then generate screens one at a time.

## Working order (important)
1. Generate ONE hero screen first: the Markets Live list (prompt S1). Iterate until the look is approved. Everything else copies it.
2. Then the stake ticket (S2) and the card states (S3).
3. Then the remaining screens in the order listed. Do not generate all screens in one go; styles drift.
4. Export to Figma (if available) so the finished frames and tokens can be handed to the coding agent.

## Plan features to verify
Public pages describe reference-image-to-design, document-to-design and Figma component import as features of higher-priced plans, and some limits on export. These are third-party descriptions; check what your plan includes before relying on them.

## Rules
Take structure, density and behavior from the references. Do not copy logos, names, icons, illustrations, wording or exact colors from any other product.
# GRM-design-
