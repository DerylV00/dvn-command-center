# DVN Life OS — Notion Setup Guide
# Build Your Visual Command Center in 30 Minutes
# Version 1.0 | April 28, 2026

---

## WHAT YOU'RE BUILDING

A Notion workspace that:
- Receives every voice dump from Optimus, auto-organized by project
- Syncs with Google Calendar so every meeting is tracked
- Connects with Fireflies so every recorded conversation is logged
- Shows a visual dashboard of your life — projects, tasks, health, finances
- Updates your live web dashboard (Netlify) automatically via GitHub

---

## STEP 1: CREATE YOUR NOTION WORKSPACE

1. Go to notion.so → sign up or log in
2. Create a new workspace: call it "DVN Life OS"
3. Create a new page called "📍 Command Center" — this is your home base

---

## STEP 2: CREATE THE 8 DATABASES

Create each database as a full-page database (not inline). Name them exactly as shown — Optimus references these names.

---

### DATABASE 1: DVN Daily Log

1. New page → "DVN Daily Log"
2. Set view to: Table
3. Add these properties:
   - **Date** (type: Date) — set as the first property
   - **Type** (type: Select) — options: 🏆 Win, 💡 Insight, 🔥 Friction, 🎯 Intention, 📋 Update, 💡 Idea
   - **Project** (type: Select) — options: Ken Alignment, Puerto Rico, Growth House, Buddy's Resort, Financial, Health, Real Estate, Library, General
   - **Entry** (type: Text) — the main content
   - **Action Items** (type: Text) — extracted action items
   - **Source** (type: Select) — options: Voice, Text, Fireflies, Manual
   - **Shadow Detected** (type: Checkbox)
   - **Shadow Type** (type: Select) — options: Key 3 Chaos, Key 13 Discord, ENFJ Overextending, Blaze Out of Genius, Drifting

4. Create these saved views:
   - "Today" — filter: Date = today
   - "This Week" — filter: Date = this week
   - "Shadows" — filter: Shadow Detected = checked
   - "Wins" — filter: Type = Win

---

### DATABASE 2: DVN Projects

1. New page → "DVN Projects"
2. Set view to: Board (grouped by Status)
3. Add these properties:
   - **Project Name** (title)
   - **Status** (type: Select) — options: 🟢 Active, 🟡 Planning, ⏸️ On Hold, ✅ Complete
   - **Priority** (type: Number)
   - **Next Action** (type: Text)
   - **Next Action Date** (type: Date)
   - **Last Updated** (type: Date)
   - **Key Numbers** (type: Text) — current stats for this project

4. Create these 8 project pages (one entry per project):
   - Ken Alignment
   - Puerto Rico Plan
   - Growth House / Immersion
   - Buddy's Resort
   - Financial Sovereignty
   - Physical Performance
   - Cove & Co. Real Estate
   - The Library

5. On each project page, add linked database views:
   - Linked DVN Tasks (filtered to this project)
   - Linked DVN Daily Log (filtered to this project)

---

### DATABASE 3: DVN Tasks

1. New page → "DVN Tasks"
2. Set view to: Board (grouped by Status)
3. Add these properties:
   - **Task** (title)
   - **Project** (type: Select — same options as DVN Daily Log Project field)
   - **Due Date** (type: Date)
   - **Status** (type: Select) — options: 📋 To Do, ⚡ In Progress, ✅ Done, 🗑️ Dropped
   - **Priority** (type: Select) — options: 🔥 Urgent, ⚡ This Week, 📋 Eventually
   - **Created** (type: Created time)

4. Create these saved views:
   - "🔥 Urgent" — filter: Priority = Urgent, Status ≠ Done
   - "This Week" — filter: Due Date = this week
   - "By Project" — group by Project
   - "All Open" — filter: Status = To Do or In Progress

---

### DATABASE 4: DVN Relationships

1. New page → "DVN Relationships"
2. Set view to: Gallery
3. Add these properties:
   - **Person** (title)
   - **Status** (type: Select) — options: 🔥 Priority Now, 🟢 Active, 🔵 Long Game
   - **Last Contact** (type: Date)
   - **Next Action** (type: Text)
   - **Next Contact Date** (type: Date)
   - **Relationship Notes** (type: Text)

4. Create entries for: Ken Wilkins, Jesse Ray, Oscar, Landen, Nathan Maurer, Rana Daggubati, Prasad Vanga, Scott Spiegel

5. On each person's page, add:
   - "Conversation Log" section — linked view of DVN Meetings filtered to this person
   - "Open Commitments" — text block, updated manually
   - "Background" — key context about the relationship

---

### DATABASE 5: DVN Financial Tracker

1. New page → "DVN Financial Tracker"
2. Set view to: Table + Chart (for the debt trend)
3. Add these properties:
   - **Date** (type: Date)
   - **Type** (type: Select) — options: 💰 Income, 💳 Debt Payment, 💸 Expense, 📈 Investment
   - **Amount** (type: Number — currency format)
   - **Category** (type: Select) — options: Buddy's Tips, Ken Role, Business Revenue, Debt Payment, BTC/Crypto, Expense, Other
   - **Notes** (type: Text)

4. Create a Chart view:
   - Chart type: Bar or Line
   - X-axis: Date
   - Y-axis: Amount
   - Filter: Type = Income or Debt Payment

5. Add a summary section at the top with these formulas:
   - Total Debt: manually updated (link to data.json)
   - Cash on Hand: manually updated
   - This Month's Income: filtered sum
   - Monthly Debt Payment Target: $1,000

---

### DATABASE 6: DVN Health Log

1. New page → "DVN Health Log"
2. Set view to: Table + Line Chart
3. Add these properties:
   - **Date** (type: Date)
   - **Weight** (type: Number) — in lbs
   - **Energy** (type: Select) — options: 🔴 Low, 🟡 Medium, 🟢 High
   - **Sleep Hours** (type: Number)
   - **Workout Done** (type: Checkbox)
   - **Protocol Taken** (type: Checkbox)
   - **Notes** (type: Text)

4. Create a Chart view:
   - Chart type: Line
   - X-axis: Date
   - Y-axis: Weight
   - This shows your transformation arc visually

---

### DATABASE 7: DVN Calendar

1. New page → "DVN Calendar"
2. Set view to: Calendar (by date) + Table
3. Add these properties:
   - **Event** (title)
   - **Date** (type: Date — with end date for multi-day events)
   - **Type** (type: Select) — options: 📞 Meeting, 🎯 Milestone, 🎪 Event, ⏰ Deadline, 🏋️ Health, ✈️ Travel
   - **Project** (type: Select)
   - **Prep Notes** (type: Text)
   - **Questions to Ask** (type: Text)
   - **Outcome** (type: Text — filled after the event)
   - **Fireflies Link** (type: URL — paste after recorded meetings)

---

### DATABASE 8: DVN Meetings
*Fireflies transcripts land here*

1. New page → "DVN Meetings"
2. Set view to: Table
3. Add these properties:
   - **Meeting Title** (title)
   - **Date** (type: Date)
   - **Duration** (type: Text)
   - **Participants** (type: Multi-select)
   - **Project** (type: Select)
   - **Fireflies Link** (type: URL)
   - **Summary** (type: Text — auto-filled from Fireflies)
   - **Key Decisions** (type: Text — extracted by Optimus)
   - **Action Items** (type: Text — extracted by Optimus)
   - **Processed** (type: Checkbox — Optimus checks this when done)

---

## STEP 3: BUILD THE COMMAND CENTER PAGE

Go to your "📍 Command Center" page and build these sections:

```
📍 DVN COMMAND CENTER
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

"Build the skills, the money, and the character —
then go back and give it."

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

[ TODAY ]
→ Linked view: DVN Daily Log — Today filter
→ Linked view: DVN Calendar — Today filter
→ Linked view: DVN Tasks — Urgent filter

[ PROJECTS ]
→ Linked view: DVN Projects — Active filter, Gallery view
→ Sort by Priority

[ KEN ALIGNMENT ]
→ Full embed of Ken Wilkins page from DVN Relationships
→ Shows: last conversation, next meeting, commitments

[ FINANCIAL PULSE ]
→ Key numbers: $33K debt, $4K cash (updated by Optimus)
→ Linked chart: DVN Financial Tracker

[ HEALTH PULSE ]
→ Key numbers: 219 lbs → 205 goal
→ Linked chart: DVN Health Log — Weight trend

[ THIS WEEK ]
→ Linked view: DVN Calendar — this week
→ Linked view: DVN Tasks — this week

[ OPEN TASKS ]
→ Linked view: DVN Tasks — open, sorted by due date, grouped by project

[ RECENT LOG ]
→ Linked view: DVN Daily Log — last 10 entries

[ LIVE DASHBOARD ]
→ Link: https://dvn-command-center.netlify.app
→ Note: auto-updates when Optimus pushes to GitHub
```

---

## STEP 4: CONNECT GOOGLE CALENDAR

1. In Notion: Settings & Members → Connections → Google Calendar
2. Click "Connect Google Calendar"
3. Sign in with your Google account
4. Select which calendars to sync (select all you use)
5. Choose "DVN Calendar" as the sync target database
6. Enable two-way sync

**What this does:**
- Every Google Calendar event appears in DVN Calendar automatically
- Events you create in DVN Calendar appear in Google Calendar
- Optimus can read your calendar to prep reminders before Ken meetings

---

## STEP 5: CONNECT FIREFLIES

### Option A — Native Fireflies Notion Integration:
1. Go to fireflies.ai → Settings → Integrations
2. Find "Notion" → click Connect
3. Authorize with your Notion account
4. Select workspace: DVN Life OS
5. Select target database: DVN Meetings
6. Enable: Auto-sync after every meeting
7. Select fields to sync: Title, Date, Summary, Transcript link, Participants

### Option B — Via Zapier/Make (more control):
1. Create a Zap: Trigger = "New Fireflies meeting completed"
2. Action = "Create new entry in DVN Meetings database"
3. Map fields: title, date, summary, transcript URL
4. Add second action: "Send message to Optimus with transcript summary"
5. Optimus processes it and routes to correct project

**Recommended format for Fireflies → Optimus:**
Tell Fireflies to send a webhook to Base.44 after each meeting.
Optimus receives: meeting title, date, duration, participants, summary.
Optimus extracts: decisions, action items, relationship updates.
Optimus logs: to DVN Meetings + DVN Relationships + DVN Tasks.
Optimus pushes: relevant updates to data.json → GitHub → Netlify.

---

## STEP 6: GIVE OPTIMUS YOUR NOTION TOKENS

1. Go to notion.so/my-integrations → Create new integration
2. Name it: "Optimus DVN Agent"
3. Select workspace: DVN Life OS
4. Permissions: Read + Write + Comment
5. Copy the Internal Integration Token
6. In Base.44 → Settings → Environment Variables:
   - NOTION_TOKEN = [paste token here]
7. For each database, go to the database → share → Invite → select "Optimus DVN Agent"
8. Copy each database ID from the URL and add to Base.44:
   - NOTION_DB_DAILY_LOG = [ID from URL]
   - NOTION_DB_PROJECTS = [ID from URL]
   - NOTION_DB_TASKS = [ID from URL]
   - NOTION_DB_RELATIONSHIPS = [ID from URL]
   - NOTION_DB_FINANCIAL = [ID from URL]
   - NOTION_DB_HEALTH = [ID from URL]
   - NOTION_DB_CALENDAR = [ID from URL]
   - NOTION_DB_MEETINGS = [ID from URL]

**How to find a database ID:**
Open the database → copy the URL
URL format: notion.so/[workspace]/[DATABASE-ID]?v=[view-id]
The DATABASE-ID is the 32-character string after your workspace name.

---

## STEP 7: TEST THE FULL SYSTEM

1. Open Base.44 (Optimus)
2. Send this test message: "log a win — I just finished setting up my Notion system. Everything is connected."
3. Optimus should:
   - Create a log entry in DVN Daily Log (type: Win, project: General)
   - Update data.json growth_log with the entry
   - Push to GitHub
4. Open Netlify dashboard — should show the new log entry within 60 seconds
5. Open Notion DVN Daily Log — should show the same entry

If all three update — the system is live. 🤙

---

## THE DAILY WORKFLOW (once everything is set up)

**Every morning (30 seconds):**
Open Optimus → "Good morning — what's on the calendar today?"
Optimus pulls from DVN Calendar and tells you the day ahead.

**After every shift, meeting, or meaningful moment (60 seconds):**
Open Optimus → voice dump → done.
Optimus routes everything, logs everything, updates everything.

**Every Sunday (5 minutes):**
Open Optimus → "Run my weekly review"
Optimus generates the summary, pushes to dashboard, asks if anything to add.

**Once a month (15 minutes):**
Come to Claude with Optimus's monthly summary.
We review the master files and update anything structural.
Paste updated files into GitHub.

---

## QUICK REFERENCE — SYSTEM DIAGRAM

```
YOU (Voice Dump / Text)
        ↓
OPTIMUS (Base.44)
    ↓           ↓
NOTION          GITHUB
(Archive)       (data.json)
                    ↓
                NETLIFY
                (Live Dashboard)

FIREFLIES → Auto-sends to Optimus after every meeting
GOOGLE CALENDAR → Auto-syncs to DVN Calendar in Notion

CLAUDE (claude.ai) ← You come here for structural work
                      Rebuilds HTML, docs, deep analysis
```

---

## TROUBLESHOOTING

**Notion not receiving entries from Optimus:**
→ Check that each database has the Optimus integration invited
→ Verify NOTION_TOKEN in Base.44 is correct
→ Check that database IDs are correct (32 characters each)

**Fireflies not syncing to Notion:**
→ Check integration is enabled in Fireflies settings
→ Verify the correct workspace and database are selected
→ Test by recording a 1-minute meeting and checking if it appears

**Google Calendar not syncing:**
→ Re-connect in Notion Settings → Connections
→ Make sure two-way sync is enabled
→ Can take up to 15 minutes for first sync

**Dashboard not updating after Optimus pushes:**
→ Check Netlify deploy log for errors
→ Verify GitHub token has correct repo scope
→ Check that data.json is valid JSON (no syntax errors)

---

*DVN Life OS Setup Guide · Version 1.0 · April 28, 2026*
*Questions? Drop a voice note to Optimus or open a Claude session.*
