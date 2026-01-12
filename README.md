# Job Search Automation – n8n Workflow

This repository contains an **n8n automation workflow** that helps automate the job search process.  
It searches for relevant job openings, processes and filters them, and saves the results into **Google Sheets** for easy tracking.

## 🔍 What This Workflow Does

1. Starts manually using **Manual Trigger**
2. Sets job search parameters:
   - Job Title: *Software Engineer*
   - Location: *Remote*
   - Keywords: *Python, JavaScript*
3. Sends a request to fetch job data (LinkedIn Jobs URL used as source)
4. Merges and processes the job data
5. Extracts important details:
   - Job Title  
   - Company  
   - Location  
   - Description  
   - URL  
   - Posted Date  
   - Salary
6. Filters only relevant roles (e.g., titles containing **“Engineer”**)
7. Saves the final results to **Google Sheets**

This creates a simple, automated pipeline for collecting and organizing job listings.

## 🛠️ Requirements

- n8n (Self-hosted or Cloud)
- Google Account (for Google Sheets integration)
- Google Sheets credentials configured in n8n

## 🚀 How to Use

1. Install and open **n8n**
2. Import the workflow:
   - Go to *Workflows* → *Import from File*
   - Select `n8n_job_search.json`
3. Configure:
   - Update job parameters in the **Active Search** node
   - Set your **Google Sheets** credentials
   - Replace `your-spreadsheet-id` with your actual Sheet ID
4. Click **Execute Workflow**
5. View the collected job data in your Google Sheet

## 📁 Files

- `n8n_job_search.json` – The complete n8n workflow export

## 🎯 Use Case

- Automating job discovery  
- Building a personal job tracking system  
- Learning real-world automation with n8n  
- Demonstrating workflow design in portfolios and resumes

---

Built by **Mohamed Irfan** as a practical automation project using n8n.
