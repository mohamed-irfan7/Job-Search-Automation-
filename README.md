Job Search Automation Workflow
An n8n workflow that automates job searching, filtering, and storing job listings from various sources.
📋 Overview
This workflow automates the process of searching for jobs, filtering them based on your criteria, and saving relevant listings to Google Sheets for easy tracking and management.
🚀 Features

Automated Job Search: Scrapes job listings from LinkedIn and other sources
Smart Filtering: Filters jobs based on title, location, keywords, and other criteria
Data Processing: Extracts and formats job details (title, company, location, salary, etc.)
Automated Storage: Saves filtered results to Google Sheets
Customizable Parameters: Easy to adjust search criteria and filters

📊 Workflow Diagram
Manual Trigger → Active Search → LinkedIn Scraper → Merge Data → Process Jobs → Filter Jobs → Save to Sheets
🛠️ Prerequisites
Before you begin, ensure you have:

n8n installed (self-hosted or cloud)
Google Sheets API credentials configured in n8n
Basic understanding of n8n workflows

📥 Installation

Clone this repository

bash   git clone https://github.com/yourusername/job-search-automation.git
   cd job-search-automation

Import the workflow into n8n

Open your n8n instance
Go to Workflows → Import from File
Select the job-search-workflow.json file
Click Import


Configure credentials

Set up Google Sheets credentials in n8n
Update the spreadsheet ID in the "Save to Google Sheets" node



⚙️ Configuration
1. Active Search Node
Update the search parameters in the "Active Search" node:
javascriptjobTitle: "Software Engineer"      // Your desired job title
location: "Remote"                 // Preferred location
keywords: "Python, JavaScript"     // Relevant keywords
2. Filter Relevant Jobs Node
Adjust filtering criteria in the IF node:
javascript// Example: Filter jobs containing "Engineer" in title
title contains "Engineer"
3. Save to Google Sheets Node

Create a Google Sheet with columns: Title, Company, Location, Description, URL, Posted Date, Salary
Update the spreadsheetId in the workflow JSON
Update the sheetName to match your sheet name

🔧 Usage

Manual Execution

Open the workflow in n8n
Click "Execute Workflow" button
The workflow will run and save results to your Google Sheet


Schedule Execution (Optional)

Replace "Manual Trigger" with "Schedule Trigger"
Set your desired schedule (e.g., daily at 9 AM)
Save and activate the workflow



📝 Workflow Nodes Explained
NodeTypePurposeManual TriggerTriggerStarts the workflow manuallyActive SearchSetDefines search parametersLinkedIn Job ScraperHTTP RequestFetches job listingsMerge DataMergeCombines data streamsProcess JobsCodeExtracts and formats job dataFilter Relevant JobsIFFilters based on criteriaSave to Google SheetsGoogle SheetsStores results
⚠️ Important Notes
LinkedIn Scraping Limitations
LinkedIn actively blocks automated scraping. Consider these alternatives:

Use Official APIs

LinkedIn Jobs API
Requires LinkedIn Developer account


Alternative Job Search APIs

Adzuna API
Indeed API
The Muse API
RemoteOK API


RSS Feeds

Many job boards offer RSS feeds
Easier to parse and more reliable



🔄 Customization Ideas

Multiple Sources: Add parallel branches for different job boards
Email Notifications: Add email node to get alerts for new jobs
Slack Integration: Send job alerts to Slack channel
Database Storage: Use PostgreSQL or MongoDB instead of Google Sheets
AI Filtering: Add OpenAI node to rank jobs by relevance
Auto-Apply: Integrate with application APIs (use with caution)

🐛 Troubleshooting
Common Issues
Issue: HTTP Request fails with 403 error

Solution: LinkedIn blocks automated requests. Use official API or alternative sources.

Issue: Google Sheets node not working

Solution: Verify credentials are set up correctly and spreadsheet ID is correct.

Issue: No jobs returned

Solution: Check your search parameters and ensure the source URL is correct.

Issue: Duplicate entries

Solution: Add a deduplication node or check existing entries before saving.

📚 Additional Resources

n8n Documentation
n8n Community Forum
Google Sheets API Docs

🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

Fork the repository
Create your feature branch (git checkout -b feature/AmazingFeature)
Commit your changes (git commit -m 'Add some AmazingFeature')
Push to the branch (git push origin feature/AmazingFeature)
Open a Pull Request

📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
👤 Author
  Mohamed irfan S

GitHub: https://github.com/mohamed-irfan7
LinkedIn: https://www.linkedin.com/in/mohamed-irfan-sb81b42299/

