# FinFlow — Finance Dashboard

A clean, interactive finance dashboard built with vanilla HTML, CSS, and JavaScript. No frameworks, no build tools — just open the file and it works.

**Live Demo:** https://poojadahiya22.github.io/finance-dashboard/
**Repository:** https://github.com/poojadahiya22/finance-dashboard

---

## What it does

FinFlow lets you track income and expenses in one place. You can see your financial summary at a glance, explore transactions, and understand your spending patterns through the Insights section.

---

## Features

### Dashboard Overview
- Summary cards showing total balance, income, and expenses with trend indicators
- 6-month bar chart comparing income vs. expenses side by side
- Donut chart breaking down spending by category
- Recent transactions table with quick navigation

### Transactions
- Full transaction list with Date, Amount, Category, Description, and Type
- Search by name or category (live filtering as you type)
- Filter by type (income/expense) and category
- Sort by date or amount (ascending/descending)
- Add, edit, or delete transactions — all saved to localStorage

### Role-Based UI (RBAC Simulation)
- **Admin role:** Can add, edit, and delete transactions. All controls active.
- **Viewer role:** Read-only mode. Add/Edit/Delete buttons are disabled and hidden. A banner clearly indicates the current access level.
- Switch roles using the toggle in the sidebar — no page reload needed.

### Insights & Analytics
- Highest spending category with total amount
- Month-over-month expense comparison (this month vs. last month)
- Savings rate (%) based on total income vs. expenses
- Average daily spend for the current month
- Total transaction count breakdown
- Largest single expense
- Category breakdown table with percentage bars

### UX & Extra Features
- **Dark / Light mode** — toggle from the sidebar, preference saved to localStorage
- **localStorage persistence** — all transactions survive page refresh
- **Responsive layout** — works on mobile, tablet, and desktop
- Smooth animations and hover states throughout
- Keyboard shortcut: `Esc` to close modal, `Ctrl/Cmd + N` to open add transaction on Transactions page
- Toast notifications for all user actions (add, edit, delete, validation errors)
- Empty state handling for filtered views with no results

---

## How to run

Just open `finance-dashboard.html` in any modern browser. No installation, no server, no npm.

```
# Option 1 — direct
Double-click finance-dashboard.html

# Option 2 — local server (if you prefer)
npx serve .
```

That's it.

---

## Project structure

```
finance-dashboard.html   ← entire app in one file
README.md
```

Everything is self-contained: HTML structure, CSS styles, and JavaScript logic in a single file. This was a deliberate choice to keep the submission simple to run and review.

---

## Tech decisions

**Vanilla JS instead of React/Vue** — The assignment said "no framework needed" and creativity in structure is what's being evaluated, not framework familiarity. Managing state with plain JS objects and localStorage keeps it simple, readable, and dependency-free.

**localStorage for state** — Transactions persist across sessions without any backend. This demonstrates practical state management thinking.

**CSS custom properties for theming** — The entire dark/light switch is handled by toggling one data attribute on the `<html>` element. Clean, zero-JS style switching.

**Role simulation on the frontend** — Roles are stored in localStorage and applied on page load/switch. The UI adapts immediately — admin sees full controls, viewer sees none. This is exactly how a real RBAC frontend layer would work before a backend enforces permissions.

---

## Assumptions made

- Currency is INR (₹). Easy to swap out.
- Seed data contains 20 realistic transactions across 3 months to make all charts meaningful from the start.
- "Insights" section extracts patterns from existing data rather than requiring user input — this felt more useful.
- The role toggle is intentionally simple and visible, since this is a demo for evaluation. In production, role would come from an auth token.

---

## What I'd add with more time

- Export transactions as CSV or JSON
- Budget targets per category with visual progress
- Date range picker for filtering
- Recurring transaction flagging
- Proper authentication layer with JWT

---

Built by Pooja Dahiya
