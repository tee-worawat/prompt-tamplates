# PRD: CodeVenture Product Analytics Dashboard  

**Product Manager:** [Your Name]  
**Engineer(s):** [TBD]  
**Stakeholders:** PMs, Business/Strategy, Leadership  

---

## 1. Introduction  

### 1.1 Purpose  
Provide PMs and stakeholders with a unified **analytics dashboard** that visualizes student engagement with `[your_product_name]`, lessons, and pages.  

### 1.2 Background  
- Analytics data exists in a `your_database` datamart and is now surfaced via a Nuxt 3 dashboard.  
- The dashboard accelerates **your_key_items (ex. retention analysis, segmentation)** by reducing manual querying.  

---

## 2. Problem Statement  
PMs/stakeholders lack a **self-service tool** to explore analytics, limiting visibility into:  
- `key analytic feature 1` 
- `key analytic feature 2`  
- `key analytic feature 3`

---

## 3. Objectives  

### 3.1 Goals  
- Ship a lightweight dashboard connected to the datamart schema.  
- Provide high‑level game analytics and summary visualizations.  
- Surface metrics: //change this to fit your requirement  
  - Entered vs Completed  
  - Completion rates  
  - Drop-offs  
  - Play percentage  
- Provide filter controls (`your filters`).  
- Provide 30‑day completion trend and time vs drop‑off insights.  

### 3.2 Non-Goals  
- Advanced segmentation/prediction
- Real-time analytics (near real-time is sufficient)
- PDF export (CSV first, if any)

---

## 4. Target Audience  
- **Primary:** Product Managers, Stakeholders.  
- **Secondary:** Leadership, Educators (summary views).  

---

## 5. Functional Requirements  

| Priority | Requirement | Description |
|----------|-------------|-------------|
| P0 | Task 1 | desc |
| P0 | Task 2 | desc |
| P1 | Task 3 | desc |
| P2 | Task 4 | desc |
| P2 | Task 5 | desc |

<!--
Putting tasks in order help the agent to prioritize
-->

## 6. Data Model Alignment  
Replace fields with your schema. Keep naming consistent across UI and API.
- Item-level: `[item_name]`, `[entered]`, `[completed]`, `[completion_rate]`, `[dropoff]`, `[play_percentage]`, `[filter_field_1]`, `[filter_field_2]`
- Trend: `{ date, avgCompletion }`

---

## 7. Success Metrics  

- ≥80% PM adoption (weekly usage).  
- 100% of games/courses in datamart accessible.  
- ≥70% reduction in manual report requests.  
- Faster iteration cycles on curriculum design (qualitative).  

---

## 8. UX / UI Draft (Wireframe + Style Guide)  

### Layout Sketch  
- Filters row with badges/counters: `your filter 1`, `...`
- KPI row (5 cards max): `kpi_1`, `...`
- Charts grid: Funnel, Drop-off, Trend, [Optional Scatter]
- Overview table


### Color Palette (Tailwind reference)  
- Primary color: `[replace with your primary]`
- Accent color: `[replace with your accent]`
- Drop-offs: `[replace with your danger color]`
- Success: `[replace with your success color]`

### Style Notes  
- KPI cards: blue accents, drop-off card in red.  
- Charts: blue gradients, red for drop-off only.  
- Icons: heroicons/lucide-react, professional (no mascots).  
- Typography: same as teacher portal (clean sans-serif).  
- Sidebar: blue tint background (`blue-50`) to differentiate from teacher view.  

---

## 9. Technical Approach  

- Frontend: [Your framework], utility CSS (e.g., Tailwind) and a charting lib (e.g., Chart.js)
- Backend: API endpoints serving aggregated metrics from your datastore
- State: One composable/store for data, filters, and trend
- Auth: [Replace with your admin auth]
- Hosting: [Replace with your hosting]

---

## 10. Open Questions  

1. Should additional filters include date range and cohorts in v1.1?  
2. Should we reintroduce lesson/page drill‑down on a dedicated route?  
3. Should we add export (CSV first) on the game table?  

---

