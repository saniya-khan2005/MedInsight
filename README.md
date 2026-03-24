Med Insight | Hospital Orchestration & Command Centre
Med Insight is a high-fidelity, data-driven Command Centre engineered for modern healthcare environments. It serves as a centralized "Operating System" for hospital administrators, aggregating real-time operational data, predictive analytics, and patient flow logistics into a unified, high-performance interface.

🚀 The Mission
Modern hospitals often suffer from "Access Block"—where patients are stuck in the ER because specialized wards are full. Med Insight solves this by providing Live Network Visibility. It allows administrators to move from reactive crisis management to proactive orchestration.

🛠️ Module Architecture
1. Med Insight (Advanced Analytics)
Purpose: Clinical outcomes, patient demographics, and stay analytics.

Key Feature: Integrates complex Excel datasets to visualize Length of Stay (LOS) trends, demographic distributions, and financial payment modes (Govt vs. Private vs. Self-Pay).

2. MedEvac Command
Purpose: Live network rerouting and ambulance dispatch simulation.

Key Feature: Tracks bed capacity across multiple hospitals. It features a dispatch engine with a JSON Persistence Layer, ensuring dispatched transfers are saved even if the system reboots.

3. Ward Capacity & Flow
Purpose: Real-time bed management across specialized departments (ICU, Cardiology, etc.).

Key Feature: Tracks the "Net Bed Change" by balancing scheduled admissions against pending discharges to prevent capacity surges.

4. Predictive Intelligence
Purpose: AI-driven demand forecasting.

Key Feature: Analyzes historical admission patterns to forecast upcoming weekly demand, allowing for optimized staff scheduling.

5. Pharmacy & Inventory
Purpose: Critical medical asset tracking.

Key Feature: Live stock monitoring with automated expiry alerts and "Days to Expiry" calculations.

💻 Technical Stack & Engineering
The Engine
Python 3.10+: Core logic and data processing.

Streamlit: High-performance web framework for the frontend.

Pandas & Openpyxl: Advanced data manipulation and multi-sheet Excel ingestion.

The Visuals
Plotly Graph Objects: Engineered dual-axis charts and responsive, theme-adaptive visualizations.

Custom CSS Layer: A handcrafted Glassmorphism UI using CSS injection to provide a premium SaaS experience.

The Architecture
Unified Design System: Centralized styling via styles.py and components.py for a consistent global look across all 9 modules.

State Persistence: Custom serialization logic using the JSON library to maintain a "Live Database" state across browser refreshes.

Safe-Mapping Data Engine: Built a resilient data-loading function that uses fuzzy matching to identify columns, preventing crashes if data formats vary.

📂 Project Structure
Plaintext
📁 med_insight_suite/
├── 📄 app.py                # Master Landing Page & Global KPIs
├── 📄 components.py         # Shared UI components (Sidebar, KPI Cards)
├── 📄 styles.py             # Global CSS & Theme definitions
├── 📄 data_engine.py        # Central Data Ingestion (Excel/CSV)
├── 📁 data/                 # Raw Datasets & Persistence Files (.json)
└── 📁 pages/                # Operational Modules (Med Insight, MedEvac, etc.)
🛠️ Installation & Setup
Clone the project folder.

Install dependencies:

Bash
pip install streamlit pandas plotly openpyxl
Launch the Suite:

Bash
streamlit run app.py
Developed for the Infosys Springboard Internship 2026 Engineering a more resilient, data-first healthcare future.
