# 🗓️ Timeline/Gantt View Component

This project implements a sophisticated, interactive **Timeline/Gantt View component**, fulfilling the requirements of the Frontend Developer Hiring Assignment.

-----

## 🎯 Objective

The primary goal was to build a production-grade, highly performant, and **accessible** horizontal time-based project visualization tool with resource allocation and task dependency features, all while adhering to a strict component architecture and design system principles.

-----

## ✨ Core Features & Implementation Highlights

| Feature | Implementation Detail | Status |
| :--- | :--- | :--- |
| **View Modes** | Supports **Day, Week, and Month** views with dynamic column scaling (`useTimeline.ts` and `position.utils.ts`). | ✅ |
| **Interactivity (D\&D)** | **Task Drag-and-Drop** (move) and **Resizing** (duration change) using low-level event listeners for performance (`useDragAndDrop.ts`). | ✅ |
| **Data Visualization** | Renders task bars, progress indicators, and resource labels. | ✅ |
| **Strict Typing** | Full implementation in **TypeScript** (Strict Mode) using defined interfaces (`TimelineView.types.ts`). | ✅ |
| **Performance** | Use of **`React.memo()`** on `TimelineRow` and `TaskBar` to prevent unnecessary re-renders during scrolling/dragging. | ✅ |
| **Scroll Sync** | Horizontal scroll is synchronized between the main task area and the $\text{TimelineGrid}$ header. | ✅ |
| **Accessibility (A11y)** | $\text{TaskBar}$ elements use `role="button"`, `tabIndex={0}`, and descriptive $\text{aria-labels}$. | ✅ |

-----

## 🛠️ Technology Stack

| Technology | Purpose | Version |
| :--- | :--- | :--- |
| **React** | Component framework | $\text{18.0.0}$ |
| **TypeScript** | Type-safe development | $\text{Strict Mode}$ |
| **Tailwind CSS** | Utility-first styling & Design Tokens | $\text{Customized v3.4.3}$ |
| **Vite** | Build Tooling & Local Server | $\text{Latest stable}$ |
| **Storybook** | Component Documentation & Demo | $\text{Latest stable}$ |

-----

## 📂 Project Structure

Key files reflect a clean, scalable component architecture:

```
src/
├── components/
│   ├── Timeline/      # Core component logic
│   │   ├── TimelineView.tsx
│   │   ├── TaskBar.tsx
│   │   └── TimelineGrid.tsx
│   └── primitives/    # Reusable UI elements (Modal, Button)
├── hooks/             # Abstraction for complex logic
│   ├── useTimeline.ts
│   └── useDragAndDrop.ts
└── utils/             # Pure calculation functions
    ├── date.utils.ts
    └── position.utils.ts
```

-----

## 🚀 Installation & Usage

1.  **Clone the Repository:**
    ```bash
    git clone [YOUR_REPO_URL]
    ```
2.  **Install Dependencies:**
    ```bash
    npm install
    ```
3.  **Run Development Server (App Preview):**
    ```bash
    npm run dev
    ```
4.  **View Storybook (Component Demo - REQUIRED):**
    ```bash
    npm run storybook
    ```
    *The component's various states (Default, Mobile View, Large Dataset, etc.) can be found in the Storybook demo.*