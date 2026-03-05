# epm-model-flowchart
Overview of the interconnected models within a typical SaaS organization. 

**Layout logic — 7 horizontal layers, information flows upward:**

Layer |Content
1. Executive | Board Reporting, Scenario/What-If
2. 3-Statement | Corporate 3-Statement (single consolidation point)
3. Corporate Finance | P&L, Cash Flow, Balance Sheet, LRP
4. Revenue & Cost Roll-ups | ARR Bridge, Bookings, Commission Accrual, Churn, NRR, AR/AP, Cloud Hosting, Vendor Cost, PS Margin
5. Functional Models | Quota & Capacity, Pipeline Gen/Attribution, Customer Health, Benefits & Comp, IT/SaaS
6. Department Models | All dept hiring plans + OpEx models
7. Foundational | Chart of Accounts, Facilities, Legal, R&D OpEx, Recruiting, Support Cost


**Interactive features:**

9 division toggles — click to isolate any division and see only its nodes + connected edges
Zoom via scroll wheel or +/− buttons
Pan by clicking and dragging the canvas
Hover any node for full description, model type, and primary outputs
Touch-friendly (pinch-to-zoom + swipe pan)


1. Click-to-isolate — Clicking any node now dims everything not directly connected to it (nodes and edges both), highlights the node itself with a glow ring, and reveals all edge labels for its connections only. Click the same node again, the background, or the "✕ Clear" button to reset. The status bar shows the selected model's name + exact input/output count.
2. Schema tooltip — Hovering any node opens a structured panel showing: division, model type, a description, and a proper Source Model → field_name → type table representing the data inputs that model consumes. This is the "Model:Field" data model view you asked for.
3. Non-overlapping labels — Labels are completely hidden in the default state (clean diagram). They only appear when a node is selected and the connected edges are highlighted. This eliminates overlap entirely while surfacing label context exactly when it's useful.
4. OpEx Aggregation as intermediate layer — The architecture was restructured so the flow is now:
Dept Models (Cloud Hosting, EPD Hiring, IT/SaaS…)
       ↓
OpEx Aggregation (R&D OpEx, G&A OpEx, COGS Rollup, S&M OpEx)  ← NEW
       ↓
Corporate P&L
These intermediate models sit at the same visual tier as the Revenue Roll-ups — both streams converge on Corporate P&L. Revenue models anchor the left side of that tier; OpEx aggregation models anchor the right, visually separating the two flows before they merge.
