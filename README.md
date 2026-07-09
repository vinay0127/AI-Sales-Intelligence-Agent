# AI-Sales-Intelligence-Agent
AI-powered Sales Intelligence Agent for Vinay Analytics Hackathon

## Project Overview

This project aims to provide sales intelligence by analyzing company profiles, recent news, and a product handbook to recommend relevant services. It uses RAG (Retrieval Augmented Generation) with an LLM to identify the best-fit services and generate actionable insights for sales outreach.

## Usage and Input

The agent is designed to be used via a Gradio web interface.

### Providing Company Inputs

You can provide company information in the Gradio UI in the "Companies" textbox:

*   **Format:** One company per line.
    *   `Company Name` (e.g., `Tata Motors`) - The agent will attempt to find a Wikipedia snippet if no website is provided.
    *   `Company Name | Company Website URL` (e.g., `Mahindra & Mahindra | https://www.mahindra.com/`) - Provides a direct website for scraping.
*   **Default Companies:** If no companies are entered, a default list of major automotive OEMs, Tier-1 Suppliers, and Component Manufacturers will be analyzed.
*   **Top K Slider:** Adjust the number of top-scoring companies to display in the UI output.

### Running the Agent

1.  Execute all cells in the notebook.
2.  The Gradio UI will launch at the end of the notebook.
3.  Enter your desired company inputs (or leave blank for defaults) and click 'Submit'.

## Generated Files

Upon execution, the agent generates the following outputs in the `/content/output/`, `/content/research/`, and `/content/outreach_emails/` directories:

*   **JSON Output:** `/content/output/sales_agent_top.json` - A JSON file containing detailed analysis for the top companies.
*   **CSV Summary:** `/content/output/top_targets.csv` - A CSV summary of the top companies, their scores, and recommended services.
*   **Market Research Report:** `/content/output/sales_agent_market_research_report.md` - A comprehensive markdown report summarizing the market analysis.
*   **Individual Dossiers Directory:** `/content/research` - Contains individual markdown files (`.md`) for each analyzed company, detailing their profile, signals, and recommendations.
*   **Outreach Emails Directory:** `/content/outreach_emails` - Contains personalized markdown email templates (`.md`) for each top company, based on the recommended service.
*   **Architecture Diagram:** `/content/architecture/architecture_diagram.png` - A visual representation of the agent's architecture.

## Architecture

(Refer to the `architecture_diagram.png` in the `/content/architecture` directory for a visual overview.)
