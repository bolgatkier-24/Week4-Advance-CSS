# SpendWise Dashboard Shell

SpendWise is a clean, modern, and fully responsive financial dashboard and budget tracker application. This project serves as the foundational capstone interface, combining modern layout engines, custom design systems, and practical expense-tracking components.

---

## 🏗️ What Was Built

This project transitions a basic flat budget tracker into a professional multi-column dashboard interface. It implements modern web design standards:
* **CSS Grid & Flexbox Layouts:** Macro-structuring via Grid and precise element alignment via Flexbox.
* **Theming & Design Tokens:** A centralized design system built on CSS Custom Properties (`:root`), complete with a dark mode override.
* **Responsive Architecture:** Fluid scaling that collapses into a single-column layout on mobile viewports (< 768px).
* **Interactive Micro-animations:** Smooth 250ms card transitions for both mouse hover and keyboard focus states.

---

## 🧩 Component Breakdown: What Each Part Does

### 1. The Dashboard Shell (`.dashboard-shell`)
* **What it is:** The root macro-layout wrapper.
* **What it does:** Uses **CSS Grid** to split the application view into a fixed-width sidebar column (`260px`) on the left and a flexible main content area (`1fr`) on the right, ensuring a professional app-like layout.

### 2. Sidebar Navigation Menu (`.sidebar`)
* **What it is:** The vertical navigation bar on the left side of the screen.
* **What it does:** Houses the brand logo (`image.png`), application title, and navigation links (*Dashboard, Transactions, Analytics, Budgets, Settings*). It uses **Flexbox** (`flex-direction: column`) to stack items vertically with clean spacing and highlights the active page.

### 3. Header Area (`.header`)
* **What it is:** The top banner of the main content workspace.
* **What it does:** Displays the page title ("Dashboard Overview"), a welcoming description, and a user profile avatar (`.avatar`). It uses **Flexbox** with `justify-content: space-between` to push the title to the left and user profile info to the far right.

### 4. Category and Metric Cards (`.dashboard-grid`)
* **What it is:** A collection of six grid cards showcasing financial metrics (*Food & Dining, Transport, Rent & Housing, Entertainment, Savings Goal, Utilities*).
* **What it does:** Built using an `auto-fit` and `minmax()` CSS Grid layout, these cards display static financial data, monetary amounts, and dynamic status tags. They feature **micro-interactions** (lifting via `translateY` and deepening `box-shadow`) that trigger within a strict **250ms** window on both mouse hover and keyboard focus (`tabindex="0"`).

### 5. Interactive Guide (`<details>`)
* **What it is:** A collapsible help section.
* **What it does:** Provides users with quick instructions on how to use the tracker without cluttering the main screen space.

### 6. Expense Input Form (`.add-expense-section`)
* **What it is:** The data-entry control center.
* **What it does:** Contains text inputs for expense names, number inputs for amounts, category dropdown selections, and an "Add Expense" button styled with focus states and interactive transition effects.

### 7. Expense Records Table (`.expenses-section`)
* **What it is:** A structured data table displaying recent transactions.
* **What it does:** Lists names, amounts, categories, and dates in rows with alternating background colors (`:nth-child(even)`) and row-hover highlights for enhanced readability.

### 8. Budgeting Tips Section (`iframe`)
* **What it is:** An embedded multimedia resource.
* **What it does:** Hosts an external YouTube educational video ("Budgeting tips for beginners") to assist users with financial literacy.

---

## 💻 Getting Started & Running Locally

1. Clone or download this project repository to your local computer.
2. Verify that `index.html`, `style.css`, and your logo asset (`image.png`) are in the **same folder directory**.
3. Open `index.html` directly in any web browser, or launch it using the **Live Server** extension in Visual Studio Code.
