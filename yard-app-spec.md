# Yard Planner App — Full Spec & Context

## Project Summary

Build a personal yard management web app for **Bruno**, a homeowner in **Washington DC (USDA Hardiness Zone 7a)**. He's starting his yard from scratch — patchy lawn, no gardening experience — and wants a visual, hands-on tool to plan, track, and manage everything. He's not a software engineer, so the app needs to be simple, intuitive, and visual-first.

The goal is a **single web app** (can be a local app, browser-based, or simple desktop app) that lets him draw his yard layout and manage everything related to keeping it healthy and growing over time.

---

## Bruno's Yard Situation (Context for the App)

- **Location:** Washington DC, USDA Zone 7a
- **Last frost:** ~April 15 | **First frost:** ~mid-November
- **Climate:** Hot, humid summers / mild winters / long spring and fall seasons
- **Soil:** Typical DC clay soil — compacted, needs compost amendment
- **Current state:** Front and back yard with patchy, unhealthy grass
- **Goals:**
  - Healthy lawn (Tall Fescue grass — the right choice for DC)
  - Native plant beds with DC-native species
  - Edible/vegetable garden (raised bed)
  - All of it looking good and growing healthy
- **Time available:** 3–5 hours/week
- **Budget:** $500–$1,000 initial investment

---

## Core App Features

### 1. 🗺️ Yard Drawing Tool (Visual Planner)
The centerpiece of the app. Bruno needs to draw his yard layout visually.

**Must have:**
- Canvas-based drawing tool to outline yard boundaries (front and back separately)
- Draw zones: lawn area, native plant beds, raised vegetable beds, paths, trees, structures (shed, fence, deck)
- Assign each zone a type/label (e.g. "Lawn," "Native Bed," "Veggie Raised Bed," "Shaded Area")
- Color-code zones by type automatically
- Add individual plant markers (dots/icons) within zones
- Sun exposure overlay: mark areas as Full Sun / Part Sun / Shade (toggle layer)
- Save and reload the drawing between sessions
- Zoom in/out on the canvas
- Simple shape tools: rectangle, freeform polygon, circle (for tree canopies etc.)
- Add labels and notes to any zone or plant marker

**Nice to have:**
- Snap to grid
- Duplicate/mirror front/back yard layouts
- Export yard map as image (PNG)

---

### 2. 🌱 Plant Database & Tracker

**Plants to pre-load in the database (from the plan):**

**Native Plants (Washington DC):**
| Name | Scientific | Sun | Type | Bloom Season | Notes |
|---|---|---|---|---|---|
| Black-Eyed Susan | Rudbeckia hirta | Full Sun | Perennial | Jul–Oct | Drought tolerant, pollinators |
| Purple Coneflower | Echinacea purpurea | Full Sun | Perennial | Jun–Sep | Attracts butterflies + goldfinches |
| Butterfly Weed | Asclepias tuberosa | Full Sun | Perennial | Jun–Aug | Monarch butterfly host plant |
| Wild Bergamot | Monarda fistulosa | Full/Part Sun | Perennial | Jul–Sep | Attracts hummingbirds |
| Little Bluestem | Schizachyrium scoparium | Full Sun | Ornamental Grass | Fall color | Turns bronze-red in fall |
| Virginia Bluebells | Mertensia virginica | Shade/Part | Perennial | Mar–May | Spring bloomer, goes dormant in summer |
| Coral Honeysuckle | Lonicera sempervirens | Full/Part Sun | Vine | Apr–Sep | Attracts hummingbirds, good for fences |
| Joe Pye Weed | Eutrochium purpureum | Full/Part Sun | Perennial | Jul–Sep | Tall (4–6ft), butterflies love it |

**Vegetables & Edibles:**
| Name | Type | Plant Time (DC) | Harvest Time | Notes |
|---|---|---|---|---|
| Lettuce mix | Cool-season | March–April | 45–60 days | Cut-and-come-again |
| Spinach | Cool-season | March–April | 40–50 days | Bolts in heat |
| Kale | Cool-season | March–April / Aug | Ongoing | Very tough, lasts through fall |
| Arugula | Cool-season | March–April | 40 days | Fast grower |
| Peas | Cool-season | March | 60–70 days | Needs trellis |
| Radishes | Cool-season | March–April | 25–30 days | Fastest vegetable |
| Cherry Tomatoes | Warm-season | After April 15 | 60–80 days | 'Sungold' or 'Sweet Million' |
| Peppers | Warm-season | After April 15 | 70–90 days | Buy transplants |
| Cucumber | Warm-season | After April 15 | 55–65 days | Train on trellis |
| Zucchini | Warm-season | After April 15 | 50–60 days | Very prolific |
| Green Beans | Warm-season | After April 15 | 50–60 days | Easy from seed |
| Basil | Warm-season | After April 15 | Ongoing | Pinch flowers to extend |
| Mint | Perennial herb | Spring | Ongoing | Plant in container — spreads aggressively |
| Thyme | Perennial herb | Spring | Ongoing | Very low maintenance |
| Rosemary | Perennial herb | Spring | Ongoing | Hardy in DC winters |

**Lawn:**
- Grass type: Tall Fescue blend
- Target height: 3–4 inches
- Mowing rule: Never cut more than ⅓ of blade height at once

**Plant tracker features:**
- Each plant in the database has: name, type, sun requirements, water needs, bloom season, planting date, location (linked to yard map zone), status (planned / planted / established / harvested / removed)
- Add custom plants not in the database
- Log planting date and mark when it germinates, blooms, produces, or is removed
- Photo log per plant (upload photos over time to track growth)
- Notes field per plant

---

### 3. 📅 Task & Seasonal Calendar

A month-by-month task calendar based on Bruno's DC Zone 7a schedule:

**Pre-loaded task schedule:**

| Month | Lawn | Vegetables | Native Plants | General |
|---|---|---|---|---|
| March | Apply pre-emergent herbicide, overseed patchy spots | Plant cool-season crops (lettuce, kale, spinach, peas, radishes) | Start sheet mulching bed areas | Soil test |
| April | Aerate, fertilize (slow-release), overseed | After April 15: plant warm-season transplants (tomatoes, peppers) | Plant natives after April 15 | Build raised bed |
| May | Mow 3–4" high, deep water 1–2x/week | Stake tomatoes, mulch bed | Mulch native beds | Add compost |
| June | Monitor for pests, keep mowing high | Harvest spring veggies, prune/deadhead | Deadhead spent flowers | Deep water |
| July | DO NOT fertilize, water deeply | Harvest tomatoes/cucumbers at peak | Water young plants | No fertilizing |
| August | Plan fall overseeding | Start fall garden seeds | Plan fall planting | Order fall seeds |
| September ⭐ | **Major overseeding** (aerate + seed + fertilize) | Plant fall crops (broccoli, kale, beets) | Plant more natives | Best lawn month |
| October | Final fertilization, mow before winter | Harvest fall veggies, cut back annuals | Leave perennial stalks standing | Plant spring bulbs |
| November–February | Nothing needed | Order seeds in January | Leave stalks for wildlife | Rest and plan |

**Calendar features:**
- Mark tasks as complete (with date completed)
- Add custom tasks with due dates and recurrence
- Upcoming task notifications / reminders (in-app or email)
- Tasks linked to specific plants or yard zones
- Weekly view + monthly view

---

### 4. 💧 Watering Tracker

- Log each watering session: date, zone/plant watered, how much (minutes or gallons)
- Target: 1 inch/week for lawn, varies by plant
- Rain integration: manually log rainfall OR connect to a weather API (like Open-Meteo, free) to auto-log rain in DC
- Water deficit indicator: shows if a zone is under/over its weekly target
- "Skip watering" button when it rained enough
- Watering schedule: set up recurring watering reminders per zone
- Visual indicator on yard map: zones that need water show up highlighted

---

### 5. 🌧️ Rain & Weather Planner

- Show a 7-day weather forecast for DC (use Open-Meteo free API or wttr.in)
- Automatically suggest "skip watering this week" when rain is predicted
- Log actual rainfall amounts (manual or API-pulled)
- Running monthly rainfall total vs. target (lawn needs ~1 inch/week)
- Frost date alerts: warn Bruno when a frost is predicted (protect tomatoes, peppers)
- Heat alerts: warn when temps exceed 90°F (affects cool-season crops, lawn stress)

---

### 6. ☀️ Sun Tracking

- Sun exposure map overlay on the yard drawing (mark zones as Full Sun / Part Sun / Shade)
- Seasonal sun angle reference: sun is lower in winter, higher in summer — show how shadows shift
- Plant recommendation filter: "What can I grow in this shaded zone?"
- Integration idea: use sunrise/sunset times for DC to calculate approximate sun hours per zone

---

### 7. 🌿 Plant Suggestions Engine

- Based on a zone's sun exposure, soil type, and purpose (ornamental / edible / lawn), suggest what to plant
- Filter by: sun level, water needs, season, native vs. edible vs. ornamental, beginner-friendly
- Each suggestion shows: photo (or emoji), name, difficulty, bloom season, planting time in DC
- "Add to my plan" button to place it directly on the yard map

---

### 8. 💰 Cost Tracker & Budget Manager

**Initial budget: $500–$1,000**

Pre-load Bruno's estimated costs from the plan:

| Item | Category | Estimated Cost | Actual Cost | Purchased? |
|---|---|---|---|---|
| MySoil Soil Test Kit | Testing | $30 | — | ☐ |
| Hand trowel + bypass pruners | Tools | $35 | — | ☐ |
| Hose + spray nozzle | Tools | $30 | — | ☐ |
| Rain gauge | Tools | $8 | — | ☐ |
| Hose timer | Tools | $25 | — | ☐ |
| Core aerator rental (1 day) | Tools/Rental | $70 | — | ☐ |
| Tall Fescue seed mix (5 lbs) | Lawn | $30 | — | ☐ |
| Compost (4–5 bags) | Soil | $50 | — | ☐ |
| Slow-release lawn fertilizer | Lawn | $25 | — | ☐ |
| Pre-emergent herbicide | Lawn | $20 | — | ☐ |
| Cedar lumber for 4x8 raised bed | Build | $60 | — | ☐ |
| Raised bed soil mix | Soil | $80 | — | ☐ |
| Vegetable transplants | Plants | $50 | — | ☐ |
| Seed packets (variety) | Plants | $30 | — | ☐ |
| Drip irrigation kit | Irrigation | $25 | — | ☐ |
| Native plants (6–8) | Plants | $80 | — | ☐ |
| Wood chip mulch | Mulch | $0–$80 | — | ☐ |

**Budget tracker features:**
- Estimated vs. actual cost comparison
- Running total spent vs. total budget
- Add new purchases with category tagging
- Filter by category (tools, plants, soil, irrigation, etc.)
- "Purchased" checkbox with date
- Budget remaining indicator
- Annual recurring cost section (things needed every year: seeds, fertilizer, mulch)

---

### 9. 🔧 Gear Inventory & Maintenance Tracker

**Pre-load Bruno's gear:**

| Tool | Status | Last Maintained | Maintenance Due | Notes |
|---|---|---|---|---|
| Weed whacker | Owned | — | — | — |
| Leaf blower | Owned | — | — | — |
| Shovel | Owned | — | — | — |
| Rake | Owned | — | — | — |
| Hand trowel | To Buy | — | — | — |
| Bypass pruners | To Buy | — | — | — |
| Hose + nozzle | To Buy | — | — | — |
| Core aerator | Rental | — | — | Rent from Home Depot |
| Hose timer | To Buy | — | — | — |
| Rain gauge | To Buy | — | — | — |

**Features:**
- Add new tools with status (Owned / To Buy / Rental)
- Log last maintenance date per tool
- Set maintenance reminders (e.g., "Sharpen mower blade every spring")
- Condition notes per tool
- Cost tracking linked to budget tracker
- Where purchased / where stored
- Estimated replacement date for consumable tools
- Weed whacker / leaf blower: log when you change the string, refuel, clean filter, etc.

---

### 10. 🧪 Soil Health Log

- Log soil test results by zone (date, pH, nitrogen, phosphorus, potassium)
- Show history of soil tests over time (is it improving?)
- Recommendations based on results: "Your pH is 5.8 — add lime to raise it to 6.5"
- Link compost/amendment applications to soil improvement tracking
- Notes field: what amendments were applied and when

---

### 11. 📸 Progress Photo Journal

- Upload photos by date and zone
- Before/after comparisons (side-by-side view)
- Seasonal photo albums (Spring 2026, Summer 2026, etc.)
- Tag photos by plant or yard zone
- Simple timeline view showing yard transformation over time

---

### 12. 📊 Dashboard (Home Screen)

The first thing Bruno sees when he opens the app:

- **This week's tasks** — what needs to happen right now
- **Weather summary** — current conditions + 3-day forecast for DC
- **Watering status** — which zones are due for water today
- **Budget snapshot** — spent vs. remaining
- **Plant spotlight** — one plant that's currently in season / needs attention
- **Quick log buttons** — "Log watering," "Log rainfall," "Mark task done"
- **Seasonal tip** — one actionable tip for the current month in DC

---

## Additional Features (Bruno's Ideas + Suggested Additions)

### Suggested by Bruno:
- ✅ Yard drawing tool
- ✅ Plan tracking
- ✅ Rain planning
- ✅ Water tracking
- ✅ Watering plants schedule
- ✅ Replant reminders
- ✅ Cost estimates
- ✅ Gear needed/owned tracker
- ✅ Gear maintenance log
- ✅ Sun tracking
- ✅ Plant suggestions

### Additional features worth adding:
- **Harvest log:** Track what you harvested and when (date, quantity, notes). Satisfying to look back on.
- **Pest & disease log:** Log any problems observed (aphids, powdery mildew, etc.) with what treatment was applied and whether it worked.
- **Seed inventory:** Track seeds you own, their expiration dates, and which ones still need to be planted.
- **Composting tracker:** If Bruno starts composting, log what goes in and when it's ready.
- **Neighbor/community notes:** Where to buy plants locally (Behnke's, Earth Sangha sales, etc.) with links.
- **Annual year summary:** At year-end, auto-generate a summary: what was planted, what succeeded/failed, total cost, lessons learned.
- **Companion planting guide:** Which vegetables grow well together (tomatoes + basil = yes; fennel + almost everything = no).
- **Fertilizer schedule:** Log when fertilizer was applied, what type, and set reminders for next application.

---

## Technical Guidance

- **Platform:** Local web app (HTML/CSS/JS) or simple Electron desktop app — Bruno just needs to open it and use it. No complex backend required to start.
- **Data storage:** JSON files stored locally, or SQLite for structured data. No cloud needed initially.
- **Weather:** Use the free [Open-Meteo API](https://open-meteo.com/) with DC coordinates (lat: 38.9072, lon: -77.0369).
- **Yard drawing:** Consider using a canvas library like Fabric.js or Konva.js for the drawing tool. Keep it simple.
- **UI approach:** Clean, visual, emoji-friendly. Not data-heavy. Bruno is a creative/visual person — it should feel like a creative tool, not a spreadsheet.
- **Mobile-friendly:** Nice to have — he may use it outdoors while working.
- **No authentication needed** — it's a single-user personal tool.
- **Offline-first** — must work without internet (except weather features).

---

## Priority Order (Build in This Sequence)

1. **Dashboard** — the home screen with weekly tasks and quick logs
2. **Seasonal Task Calendar** — pre-loaded with DC Zone 7a schedule, mark tasks complete
3. **Plant Tracker** — add/manage plants with planting dates, status, notes
4. **Watering Tracker** — log watering + rainfall, see what's due
5. **Budget Tracker** — spending vs. budget, pre-loaded items
6. **Gear Tracker** — owned/needed tools, maintenance log
7. **Yard Drawing Tool** — the visual map (most complex, save for when basics work)
8. **Sun Tracking overlay** — add on top of drawing tool
9. **Weather Integration** — pull DC weather via Open-Meteo API
10. **Plant Suggestions Engine** — filter/recommend plants
11. **Soil Health Log** — track test results over time
12. **Progress Photo Journal** — visual timeline
13. **Additional features** — harvest log, pest log, seed inventory, etc.

---

## Data Context: Bruno's Starting Point

Here's the initial data to pre-populate the app with when it first launches:

**Yard Zones (to be drawn/adjusted by Bruno):**
- Front Yard: Patchy lawn (Tall Fescue target), planned native plant beds
- Back Yard: Patchy lawn (Tall Fescue target), planned raised vegetable bed (4x8 ft), planned native plant beds

**Current month:** March 2026

**Immediate tasks (pre-load these as the first to-do items):**
1. Buy soil test kit (MySoil) and test front yard, back yard, and veggie bed area
2. Clear yard debris (use weed whacker + leaf blower)
3. Apply pre-emergent herbicide (crabgrass prevention — do before April)
4. Plant cool-season vegetables: lettuce, spinach, kale, peas, radishes, arugula
5. Start sheet mulching for native plant beds (lay cardboard + wood chips now)
6. Build 4x8 cedar raised bed in sunniest spot in backyard

**Key dates (DC Zone 7a):**
- Last frost: ~April 15, 2026
- Warm-season planting starts: April 15, 2026
- Best lawn overseeding window: September 1–30, 2026
- First frost: ~November 15, 2026

---

*Generated from a gardening planning conversation. All plant data, timing, and costs are tailored to Washington DC (USDA Zone 7a) and Bruno's specific yard situation.*
