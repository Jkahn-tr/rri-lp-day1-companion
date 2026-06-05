# Love & Passion Weekend — Day 1 Digital Companion
## Prototype Concepts + Creative Brief
*Prepared for Pam Hendrickson · June 2026*

---

## Section 1: What You're Looking At

The `index.html` file is a fully clickable, 14-screen prototype of the Day 1 digital companion for Love & Passion Weekend (Friday, September 25, 2026). It walks participants through the evening in Tony's exact sequence — from arrival through the vision write-outs, to the payoff screen where their own words are reflected back.

**What's locked in this prototype:**
- Linear, forward-only navigation (tap Continue, no menu)
- Tony's exact language verbatim in every quote and write-out prompt
- The 6 Positions framework and grid (tap to select, auto-advances)
- Three vision write-out fields that persist across the session (localStorage)
- End-of-day vision payoff screen that assembles participant's own text
- Tony AI placeholder card with alert explaining the full integration
- Color arc: warm amber arrival → deep rose deepening → midnight blue close

**What's flagged for Pam's review (four items — flag badges visible on screen):**
- **S2:** Intention write-out prompt — creative addition, not Tony's language
- **S9:** Honest Question prompt — adapted from transcript, combined two moments; confirm exact phrasing
- **S12:** Love Note screen — creative addition from brief's seeds section; approve or cut
- **S13:** Close line "You showed up. That matters." — connective copy, not Tony/Sage; approve or replace

**What's deliberately not built yet:**
- Progressive unlock (all 14 screens are accessible now — production locks them in step with the room)
- Cloud persistence (prototype uses localStorage only — clears on device switch)
- Real Tony AI conversation
- Partner send (Love Note screen shows a modal placeholder)
- SuisseIntl fonts (prototype uses Georgia + system sans)

---

## Section 2: What This Builds On — Justin's BM Work

**What carries forward from the BM digital manual:**

| Element | BM Manual | LP Day 1 Companion |
|---|---|---|
| Mobile-first layout | ✓ | ✓ |
| Auto-save feel | localStorage | localStorage (same pattern) |
| Fixed progress bar | ✓ | ✓ |
| Bottom nav bar | ✓ | ✓ |
| Warm, premium aesthetic | Cream + gold + emerald | Dark + gold (different register) |
| Single-column clarity | ✓ | ✓ |
| Entrance animations | ✓ | ✓ |

**What deliberately changes, and why:**

The BM manual is content that lives on a page — participants go in, read, fill, navigate. That's exactly right for a manual.

The relationship companion is not a manual. It's a room companion — it lives alongside a live event where Tony Robbins is on stage. Every design decision flows from one constraint: *it cannot pull attention from the room.* That produces a fundamentally different experience:

- **One thought per screen.** Not one module — one thought. A quote gets its own screen. A bridge ("Tony is about to begin.") gets its own screen. If there's more than one thing on a screen, someone's reading instead of listening.
- **Locked linear flow.** No module menu. No skip. No "explore." The participant goes where Tony sends them and nowhere else.
- **Emotion-first, capture second.** The BM manual is heads-down. This companion is heads-up — most screens have nothing to do except receive one idea or be reminded to be present.
- **Color shifts with the room.** Warm amber for arrival, deep rose for the emotional deepening section, midnight blue for the late-night vision work. The app feels different at 10 PM than at 7 PM — intentionally.
- **Dark background.** BM's cream-and-green is perfect for a workbook read at a desk. This companion is used in low light, in bed, on the couch after a long emotional session. Dark and still is right here.

---

## Section 3: The 3 UX Concepts

---

### CONCEPT A — The Still Canvas

**Philosophy:** Maximum restraint. Every screen is treated like a gallery wall — one object, nothing else. If a screen can't justify every element on it, those elements are cut. The stillness is the design.

**Key design decisions:**
- No transitions between screens — hard cuts only. The change itself is the punctuation.
- Typography does all the emotional work: weight, size, spacing, Georgia italics at large sizes
- No background color variation — one dark, unchanging field the entire evening
- Write-out prompts appear exactly as Tony spoke them, no framing copy, no instructions
- The payoff screen surfaces text in near-silence — no labels, just the words

**Emotional effect:** Gravitas. Intimacy. Ceremony. Every screen feels important because nothing is wasted.

**✓ Works well for:**
- Respecting Tony's words — they land without framing
- Participants who are emotionally in it — they don't need context
- The quote moments (S4, S5) — a single quote on a still screen is a full moment

**✗ Tradeoffs:**
- May feel cold or sparse to participants expecting guidance
- No wayfinding — participants may feel lost between sections
- The write-out screens need *some* instruction; too bare may produce blank fields

---

### CONCEPT B — The Companion Journey

**Philosophy:** Light/dark toggle — dark mode for receiving (videos, listening, emotional moments), cream mode for writing and reflecting. The app adjusts its register to what the participant is doing. Builds most directly on the BM aesthetic.

**Key design decisions:**
- Cream background on all write-out screens (S8, S9, S10, S12) — warmer, more like paper, easier to write on
- Dark background for bridge, quote, and payoff screens — receiving mode
- The toggle happens automatically on screen change (no user control needed)
- SuisseIntl + Georgia combination (BM's Fraunces replaced with Georgia for serif warmth)
- Slightly more instruction copy on write-out screens — enough to orient without teaching

**Emotional effect:** Familiar, warm, trustworthy. The cream moments feel like writing in a journal. The dark moments feel like a cinema.

**✓ Works well for:**
- Participants who respond well to the BM aesthetic (cream = home, safe, Tony's brand)
- The write-out experience — cream on a blank page signals "write here"
- Differentiation between receiving mode and capture mode

**✗ Tradeoffs:**
- Background switching may feel jarring if not executed precisely
- More visual complexity — two visual registers to maintain consistently
- Could feel slightly inconsistent with the late-night emotional atmosphere

---

### CONCEPT C — The Breathing Room *(prototype built in this direction)*

**Philosophy:** Motion as emotion. The background color shifts barely-perceptibly across the 3-hour evening — warm amber on arrival (6:30 PM) → deep rose as Tony goes into love and fear and generous lover (8 PM) → midnight blue as participants move into their vision write-out (9 PM). No screen announces this shift. Participants feel the evening change without being told it's changing.

Every screen remains minimal — Concept A's radical restraint applies fully within each screen. But the whole evening has a felt arc.

**Key design decisions:**
- Three background states with 2.5-second CSS transitions between them — the shift is perceptible but not distracting
- `#110E0A` (warm amber-black) → `#120A0C` (deep rose-black) → `#080B14` (midnight blue-black)
- All three states are very dark — the contrast between them is felt in the body, not read in the eye
- Section tag (top right) quietly names the current segment — the only wayfinding
- Gold accent (#B8895A) reads differently against each background: warmer in amber, richer in rose, cooler in midnight — the same color does emotional work across the arc

**Emotional effect:** Participants sense the evening deepening without being aware of a "feature." The room and the companion feel in sync. The vision write-outs feel like late-night work — quiet, candlelit, private.

**✓ Works well for:**
- The full evening arc — the companion has a beginning, middle, and end that participants feel
- Quote moments in rose — the color makes the emotional content land differently
- Vision payoff at midnight blue — the reflective register matches what just happened in the room
- Doesn't require any participant decision-making (it just is)

**✗ Tradeoffs:**
- The background shifts are subtle — some participants may not notice or care (that's fine, it still works)
- Three dark backgrounds are very similar — on OLED screens, perfect; on cheaper LCDs, the differences may compress
- Requires careful production timing if the companion is ever programmatically unlocked to match the room clock

---

## Section 4: What the Prototype Demonstrates

This prototype is built in the direction of **Concept C — The Breathing Room**, combined with **Concept A's radical restraint per screen**.

**What works in this prototype:**

- **The emotional arc lands.** Open the prototype and tap through the quote screens (S4, S5). A single Tony quote on a still dark screen with a narrow rule is a complete moment — not a slide, not a content card. A moment.
- **The vision payoff works.** Fill out the three write-out screens (S8, S9, S10), then advance to S11. Your own words appear assembled as your vision. If you left them blank, placeholder text shows in the empty state. The emotional logic is sound.
- **The positions grid is clean.** Tap a card — it selects and auto-advances after 480ms. Private, fast, no drama.
- **Tony's words are verbatim throughout.** No paraphrasing. No synonyms. Exact.
- **Flag badges are visible.** Pam cannot miss the four items flagged for review.

**What's deliberately not built yet (production gaps):**

- Progressive unlock (screens unlock in step with the room, not all at once)
- Cloud save (localStorage only — participant loses work on device switch)
- Real Tony AI conversation
- Partner message send
- SuisseIntl font (production will swap Georgia for SuisseIntl per brand)
- Facilitator dashboard (to see which participants are where in the flow)

---

## Section 5: Day 1 Screen Map

| # | Screen | Unlocks When | What's On Screen | Language Source | Notes / Flags |
|---|---|---|---|---|---|
| S0 | Splash | Immediately | "Foundation & Vision / Day 1 / Friday Sept 25 / with Tony & Sage Robbins" | Connective | Entry point |
| S1 | Welcome | On tap | "Something brought you here tonight." + orientation body text | Connective | Sets the register — brief and warm |
| S2 | Intention | On tap | Write-out: "The one thing I most want to feel this weekend is —" | ⚑ **My writing, not Tony's** | Creative addition; flag visible; approve or replace |
| S3 | Bridge — Intro | On tap | "Tony is about to begin." / "Be in the room." | Connective | Sends participant back to the room |
| S4 | Quote — Oxygen | On tap | "Love is the oxygen of life." — Tony Robbins | **Verbatim** (transcript p. 10) | Background shifts to rose here |
| S5 | Quote — Generous Lover | On tap | "What would a totally generous lover do for the one that they adore…" — Tony Robbins | **Verbatim** (transcript p. 16) | |
| S6 | 6 Positions | On tap | 2×3 grid of position cards; tap selects + auto-advances | **Verbatim labels** (Tony's framework) | Private. Saved to localStorage. |
| S7 | Bridge — Vision | On tap | "Tony is about to lead you into your vision." / "Let his questions land." | Connective | Sends participant back to the room before write-outs |
| S8 | Write-Out 1 | On tap | "Describe it. What's this relationship all about? Who will it inspire…" — Tony Robbins | **Verbatim** (transcript p. 297) | First vision write-out |
| S9 | Write-Out 2 | On tap | "And then if you dare to be honest — what's gotten in the way of this vision…" — Tony Robbins | ⚑ **Adapted** — two transcript moments combined | Source text: "if you dare to be honest about why that vision has not yet been realized and what you can do to change it" — condensed for screen. Pam: confirm phrasing or revert to exact. |
| S10 | Write-Out 3 | On tap | "What's most important to you in this relationship? What do you want to bring to it…" — Tony Robbins | **Verbatim** (transcript p. 300) | |
| S11 | Vision Payoff | On tap | Participant's own text assembled as "Your Vision · Day 1" / Tony AI card | Participant's words | **"Digital Fred" note:** The master calendar marks the Vision segment "with Digital Fred." Unclear what Digital Fred is — if it's an existing digital tool (AI facilitator? separate app?), the vision capture screens may need to integrate with or replace it. Flag for Pam. |
| S12 | Love Note | On tap | "Something you want to say to the person you love." / textarea / send or keep private | ⚑ **Creative addition** | From brief's seeds section. Bold idea — may not fit every attendee situation. Approve, modify, or cut. |
| S13 | Close | On tap | "✦ ✦ ✦ / Day 1 · Complete / You showed up. That matters." / Day 2 teaser | ⚑ **Close copy is mine** | "You showed up. That matters." is connective copy — replace with Sage/Tony close if there's a preferred evening close. |

---

## Section 6: Tony AI Integration Map

### Guiding principle

Tony AI lives in the companion — not in the room. It never competes with live Tony. It surfaces at rest, not during high-state moments. When in doubt: not yet.

### Where it appears

**1. Vision Payoff — S11 (Primary, highest value)**
After participants have written their vision across three prompts, the payoff screen assembles their words and offers a Tony AI card. The participant's written entries are passed as context.

What Tony AI does here: engages directly with the participant's own vision — not with generic relationship content. It might surface a pattern, ask what's underneath, or offer the one question that opens it further.

Why this works: the participant just did significant emotional work. They've written their vision. They're ready for a response that reflects it back at them — not a summary, a question. High-value, high-timing.

**2. End of Day — S13 (Secondary, light touch)**
Not a conversation. One quiet question before sleep — something like "What's one thing you want to hold onto from tonight?" The participant doesn't respond; the question lands and the screen closes. Tony AI as a still moment, not a dialogue.

Why this works: the evening is ending. The emotional register is close, not open. One question is the right weight.

### Where it's scoped but out of range for Day 1

**3. Day 2 morning nudge (out of scope for Day 1 — flag for Day 2 build)**
Tony AI sends a personalized message the morning of Day 2 using the participant's Day 1 vision as context. "Last night you wrote [X]. Today we go into patterns. Here's what I'd hold onto." This requires cloud persistence (the Day 1 write-outs must be server-side for this to work).

### Where Tony AI does NOT appear

- **During video segments** (S3, S4, S5, S7 — participant is watching Tony live or on video)
- **During the 6 Positions** (S6 — private, reflexive moment; AI would interrupt it)
- **During write-out screens** (S8, S9, S10 — the writing is the moment; AI competes)
- **Facilitator/breakout periods** — no app use at all is preferred during live facilitation

### Integration notes for production

- Tony AI needs read access to the participant's write-out fields (vision1, vision2, vision3) as prompt context
- The conversation should feel like Tony's voice — not an AI assistant. Brand voice rules from the brief apply fully.
- The Vision Payoff AI conversation is the killer feature. Build that first.
- Consider session memory: Day 1 vision context should carry into Days 2 and 3

---

## Section 7: Creative Additions Flagged for Review

These four items appear with visible flag badges in the prototype. Pam: these require a decision before production.

---

**⚑ S2 — Intention write-out**

> *"The one thing I most want to feel this weekend is —"*

This is my writing, not Tony's. It sets a personal intention before the evening starts — a quiet moment of self-orientation before Tony takes the stage.

**Why it's here:** The brief's brief asks for moments that hold the emotional arc, and arrival anxiety is real. This gives participants something to do with that energy. It also seeds a personal stake they'll carry into the write-outs.

**Pam's decision:** Approve as-is / modify the prompt / replace with a Tony quote that sets arrival intention / cut entirely.

---

**⚑ S9 — The Honest Question**

> *"And then if you dare to be honest — what's gotten in the way of this vision, and what are you going to do differently?"*

Source text from transcript (paragraph 297): *"And then if you dare to be honest about why that vision has not yet been realized and what you can do to change it."*

This is a condensed adaptation — two of Tony's ideas are joined ("dare to be honest" + "what you can do to change it"), the phrasing slightly tightened for a screen.

**Pam's decision:** Approve adaptation / revert to transcript verbatim / provide alternate source text. Do not leave as-is without confirmation — Tony's exact words are the standard.

---

**⚑ S12 — Love Note**

> *"Something you want to say to the person you love. It doesn't have to be big. Sometimes it's three words."*

This is a creative addition drawn from the brief's seeds: *"Connection to their partner. For people attending in a relationship, moments to write a love note, send a message to their partner."*

The screen has two actions: "Send it tonight →" (prototype shows a modal explaining the feature) and "Keep it private" (advances without sending).

**Why it's here:** It's the one screen in the companion that turns inward reflection into outward action — before bed on Day 1, write something to the person you love. The brief specifically called this out as a seed. It lives at the right moment (post-vision, pre-sleep).

**Pam's decision:** Approve / modify / cut. If approved, production needs: a send mechanism (SMS, email, or in-app), and a decision about attendees who are single (the current phrasing — "the person you love" — works for solo attendees as a self-directed note if needed).

---

**⚑ S13 — Close copy**

> *"You showed up. That matters."*

This is my connective copy, not a Tony or Sage close. It's intentionally brief — one line, no explanation.

**Pam's decision:** Approve as-is / replace with a Tony or Sage close from the program / expand with a preferred closing sentiment. If there's a preferred program close (a line Sage uses, or a Tony signoff), that should replace this.

---

## Section 8: Production Notes

**Progressive unlock.** In production, screens unlock in step with the room — participants should never be 20 screens ahead of Tony. Recommended approach: a facilitator control panel (or time-based unlock keyed to the session schedule) releases each screen block as Tony advances. The companion receives the unlock via a lightweight push (WebSocket or polling).

**Cloud save.** localStorage-only is adequate for a prototype but not for a launch. Participants lose their work on device switch (phone to tablet, incognito mode, etc.). Production requires server-side persistence keyed to participant account — this is also the prerequisite for the Day 2 morning nudge and the Tony AI vision context.

**Fonts.** Prototype uses Georgia (serif) + system sans. Production uses SuisseIntl (11 variants on Mac mini — files confirmed available). SuisseIntl Light at 300 weight will replace body-text instances; SuisseIntl Regular will handle eyebrows and attribution. Georgia remains for all quote and prompt text (editorial serif is right for Tony's voice at those sizes).

**Vision payoff — persistence.** The payoff is currently assembled client-side from localStorage. Production needs server-side field values: (a) if participant switches devices, their vision should still appear; (b) Tony AI needs to read these fields from the server, not the browser.

**"Digital Fred" — open question.** The master calendar marks the vision segment as "with Digital Fred." This phrase is not explained anywhere in the brief or calendar. Possibilities: an AI facilitator tool Tony uses on stage, a separate companion experience, a code name for this project, or a specific digital vision-writing tool already in use. If Digital Fred is an existing tool, the vision capture screens (S8–S10) may need to integrate with it or deliberately replace it — either way, this needs clarification before production.

**The 6 Positions — position data.** Currently saved to localStorage as a number (1–6). In production, this feeds Tony AI context and potentially the facilitator dashboard. Design decision needed: does the facilitator see aggregate position data across the room, or is this permanently private to the participant?

**Day 2 scope.** The close screen (S13) already teases Day 2. Production will add a Day 2 companion (Patterns & Seasons, Saturday September 26). The Day 1 vision write-outs should be readable in Day 2 as context — design the data schema with this in mind from the start.

---

*Built with source files: Day 1 Companion Agent Prompt, Platinum Relationship Tulum 2025 Transcript, L&P Master Calendar V2, BM Digital Manual reference.*
*Prototype direction: Concept C — The Breathing Room.*
*Tony's exact language sourced verbatim from transcript wherever used.*
