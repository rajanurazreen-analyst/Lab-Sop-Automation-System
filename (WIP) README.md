⚠️ Note: This project is currently a Work in Progress. I am documenting the automation logic and sanitizing the data templates for public viewing

# Lab-SOP-Automation-Inventory
Lab Automation for Expiry Records

Project Overview
This project solves the challenge of manual document tracking in a regulated laboratory environment. By integrating with readily software such as Microsoft Excel and Power Automate, I developed an automated system that monitors Standard Operating Procedure (SOP) expiry dates and sends proactive email notifications to stakeholders, ensuring 100% compliance with minimal manual oversight.


The Problem
In a high-compliance laboratory setting, tracking hundreds of SOPs manually using a spreadsheet is high-risk.


Risks: Human error in checking dates, missed expiry deadlines, and potential audit non-compliance
Infrequency: Manual checks were only performed weekly, leading to a reactive rather than proactive workflow

	
Tech Stack
Data Management: Microsoft Excel (Table-based tracking)
Automation: Power Automate (Cloud Flows)
Communication: Microsoft Outlook/Teams

	
The Solution:
I desgined a workflow as following:
1. Centralized Database : An Excel table stores SOP metadata (ID, Title, Owner and expiry_date)
2. Daily Trigger: A Power Automate flows runs every morning to scan the table
3. Conditional Logic: The system calculates the difference between Today() and the expiry_date
4. Tiered Alerts:
   - 30 Days Prior: Sends an intitial 'Review Required' email to the SOP owner
   - 7 days Prior: Sends a 'Final Warning' alert
   - Expired: Flags the status as 'Non-compliant' in the master list.

Workflow Visualization
(WIP)

Impact and Results
-Efficiency : Eliminated 2 hours of manual verification per month
-Compliance: Reduced missed review deadlines to 0%
-Scalability: The system can be easily expanded to track equipment calibration, inventory tracking or staff training records.

Repository Structure
- SOP

