# Rules: CodeVenture Analytics Dashboard

## Tech Framework
- **Frontend:** Nuxt 3 (Vue 3 + Vite)
- **Styling:** TailwindCSS
- **Charts:** Chart.js (registered via client plugin)
- **Icons:** lucide-vue or heroicons
- **Components:** Custom `UiCard` and analytics components in `components/analytics`
- **Data:** Read from MongoDB datamart via Nuxt server API endpoints
- **Auth:** Integrate existing CodeVenture admin auth (placeholder in layout for now)

## Layout Conventions
- Sidebar navigation: fixed left, width `280px`, branded background, links with active state
- Top KPI row: responsive grid, up to 5 cards
- Tables: custom table inside `UiCard`
- Charts: wrapped in `UiCard` with title + chart area
- Color palette:
  - Primary Blue: `blue-600`
  - Secondary Indigo: `indigo-700`
  - Neutral Gray: `gray-500`
  - Drop-offs: `red-500`
  - Completion Success: `emerald-500`

## File Structure
- `pages/analytics-dashboard.vue` → Main dashboard
- `layouts/analytics.vue` → Global layout with sidebar
- `plugins/chartjs.client.ts` → Chart.js registration
- `composables/useAnalytics.ts` → Data, filters, trend
- `components/analytics/KpiCard.vue` → KPI cards
- `components/analytics/GameTable.vue` → Game overview table
- `components/analytics/FunnelChart.vue` → Funnel chart
- `components/analytics/DropoffChart.vue` → Drop-off chart
- `components/analytics/CompletionTrend.vue` → Trend chart
- `components/analytics/TimeVsDropoffScatter.vue` → Scatter chart

## Development Rules
- Start with **mock data** from schema before API wiring
- Favor **high-level summary** on dashboard; drill-down can live on dedicated routes
- Keep **professional blue theme** distinct from teacher portal
- Consider **CSV export** as a follow-up; PDF optional later
- Keep responsive; ensure sidebar and cards look good on mobile
