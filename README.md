<!-- Paste this HTML into LinkedIn's post editor (or use it as a reference for formatting) -->
<div style="font-family: Arial, Helvetica, sans-serif; line-height:1.45; color:#111;">
  <h1 style="margin:0 0 8px 0;">Multi-Level OOPS ALV Drilldown Report in ABAP</h1>
  <p style="margin:0 0 12px 0; font-weight:600;">(PO → Items → Schedule Lines)</p>

  <p>I built a <strong>3-level drilldown ALV report</strong> in ABAP using an OOPS architecture, dynamic selection-screen behavior, and double-click navigation. I’ll attach the working video, screenshots and full code in this post.</p>

  <h2 style="font-size:16px; margin-top:18px;">🔍 Key Features</h2>

  <h3 style="margin:12px 0 6px 0;">1) Three-Level ALV Drilldown</h3>
Level 1: EKKO
• PO Header Data
• Action: Double-click to load EKPO items

Level 2: EKPO
• PO Item Details
• Action: Double-click to load EKET schedule lines

Level 3: EKET
• Schedule Line Data
• Action: Final drilldown view (no further navigation)

All three ALVs are displayed on one screen for a clean, seamless user experience.

  <h3 style="margin-top:14px;">2) Smart Selection Screen</h3>
  <ul style="margin:8px 0 0 18px;">
    <li><strong>Default Date Range:</strong> Automatically shows last 90 days</li>
    <li><strong>Date Validation:</strong> Warns if the date range exceeds 90 days</li>
    <li><strong>Checkbox-Controlled Fields:</strong> A checkbox toggles additional date fields (enabled/disabled dynamically)</li>
    <li><strong>Live Screen Modification:</strong> Selection-screen fields hide/show instantly using <code>MODIF ID</code></li>
  </ul>

  <h3 style="margin-top:14px;">3) Smooth OOPS-Based Navigation</h3>
  <ul style="margin:8px 0 0 18px;">
    <li><strong>Event Handler Classes:</strong> Capture double-click events for each ALV</li>
    <li><strong>Dynamic ALV Refresh:</strong> Child ALV updates instantly based on selected row</li>
    <li><strong>Dedicated Field Catalogs:</strong> Clear separation for EKKO, EKPO, EKET</li>
    <li><strong>3 Custom Containers:</strong> CC1, CC2, CC3 — each holds one ALV</li>
  </ul>

