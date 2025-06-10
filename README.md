# Visual MES Demo - Allegion Steelcraft

This is a single-file, interactive web application designed to simulate a Manufacturing Execution System (MES) whiteboard for the Allegion Steelcraft hollow metal door frame production line.

It provides a visual, drag-and-drop interface to track orders through various production stages, from initial receipt to final shipping. This tool serves as a functional prototype to demonstrate the core value of real-time visibility and centralized production tracking, which can be achieved with a "Manual MES" pilot or a full digital MES implementation.

## Features

-   **Visual Production Board:** A Kanban-style board with columns representing each key stage of the door frame manufacturing process.
-   **Order Management (CRUD):**
    -   **Create:** Add new orders with details like Order Number, Customer, Frame Type (K/D or FW), and special notes.
    -   **Read:** View all orders and their current status at a glance.
    -   **Update:** Edit the details of any existing order.
    -   **Delete:** Remove orders from the board.
-   **Drag & Drop Functionality:** Easily move orders between production stages by simply dragging and dropping the cards. The system state is updated automatically.
-   **Visual Cues:**
    -   **Rush Orders:** Marked with a prominent red border for immediate identification.
    -   **Frame Type Tags:** Color-coded tags clearly distinguish between **K/D (Knock-Down)** and **FW (Full Weld)** orders.
-   **Self-Contained & Zero-Dependency:** The entire application is contained within a single `MES_demo.html` file. It requires **no internet connection, no server, and no setup**. It runs directly in any modern web browser.
-   **Responsive Design:** The layout is functional on various screen sizes, though it is optimized for desktop viewing to simulate a large-scale board.

## Purpose & How to Use in a Presentation

This application is a powerful tool for demonstrating the "why" behind an MES proposal. Instead of just talking about concepts like "visibility" and "bottleneck identification," you can show them in real-time.

1.  **Introduce the Current State:** Explain the challenges of the paper-based traveler system (lost papers, no real-time status, etc.).
2.  **Present the "Manual MES" Concept:** Describe the idea of a physical whiteboard.
3.  **Demo the Application:**
    -   Open `MES_demo.html` in a web browser on the presentation screen.
    -   **Show a "Day in the Life":**
        -   Click "**+ Add New Order**" to simulate a new order coming in from the ordering system. Fill out the details for a "Rush" order. Show how it appears instantly in the "Orders Received" column.
        -   **Drag the new order** to the "Shearing" column, explaining, *"The shearing operator has just picked up this job."*
        -   **Drag another card** from "Punching" to "Press Brake," explaining how this provides an instant, accurate status update for anyone on the floor or in the front office.
    -   **Demonstrate Bottleneck Identification:** Drag several cards into one column (e.g., "Press Brake"). Point to the screen and say, *"At a glance, we can see there's a pile-up at the press brake. This allows our supervisors to react immediately—maybe by reallocating labor or adjusting the schedule—instead of finding out hours later."*
    -   **Show the Value of Data Accuracy:** Click the "Edit" icon on a card to fix a typo or update details. Contrast this with the difficulty of correcting information across multiple paper travelers.

## How to Run

1.  Download or copy the code from the `MES_demo.html` file.
2.  Save the code as a file named `MES_demo.html`.
3.  Open the `MES_demo.html` file in a modern web browser (e.g., Google Chrome, Mozilla Firefox, Microsoft Edge, Safari).
4.  That's it! The application will be fully functional.

## Technical Details

The application is built using standard web technologies:

-   **HTML:** Structures the content of the page.
-   **CSS:** Styles the application for a clean, professional look and feel, including the "Allegion Blue" branding.
-   **JavaScript (Vanilla):** Powers all the interactivity, including:
    -   DOM manipulation to render the board and cards.
    -   Event handling for button clicks and drag-and-drop actions.
    -   State management via a simple `orders` array object, acting as the single source of truth for the application.

There are no external libraries or frameworks, ensuring maximum portability and simplicity. The order data is stored in-memory and will reset upon browser refresh, which is ideal for demonstration purposes.
