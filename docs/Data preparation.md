Data used for this project were downloaded from three sources:  Google Analytics, CiviCRM and SAcommunity. Below are the procedure to download these data.
The traffic metrics (sessions, views) are obtained from Google Analytics, while CiviCRM and SAcommunity (Data.Gov.au export) data are used to produce a single master list of all organisations in SAcommunity for this council. 
___
## Google Analytics data
1. Login Data Studio (new name of Looker Studio) https://datastudio.google.com/u/0/navigation/reporting using your personal google account that linked to SAcommunity/had permission to use Google Analytics to get data from SAcommunity.
2. Crate a blank report, click on Google Analytics, then choose https://sacommunitry.org-GA4
3. Add "Landing page + query string" to Dimension and "Active users", "New users", "Sessions", "Views", "Total users" to Metric.
	- Search and drag "Landing page + query string" from Data board on the right to the white board on the left,  
	- then you could see it at Chart Board on the right under Dimension section,  
	- then Click "Add Metric" and Search for "Active users", "New users", "Sessions", "Views" under Metric Section.
4. Set the Default date range to custom and choose the data you want.(Financial Year: 1 Jul - 30 Jun; Calendar Year: 1 Jan - 31 Dec).
5. Click on the graph, then click on More(or Right Click), select Export, export as CSV (Excel).
6. Open the file then save the file as FY_GA4_All year.xlsx format, e.g., 25_26_GA4_All year.xlsx.
___
## Data.Gov.au data 
1. Start by logging into SAcommunity and go to  [https://sacommunity.org/export](https://sacommunity.org/export).
2. Select Data.Gov.au export from the available options and with the Datasets tab select the council for which the report would be generated e.g. Holdfast Bay. Then **click Export**.
3. **Click on Link or copy** the link and paste it in a new tab to download the export. The file will be automatically downloaded.
4. Lastly open the csv file and then click on save as "Excel workbook" with the extension .xlsx and rename the file to follow the format  CouncilName_FinancialYr_DataGov_export.xlsx, e.g., Holdfast Bay Council_25_26_DataGov_export.xlsx.
--- 
## CiviCRM data
1. Click on **CiviCRM Admin** tab on top of SAcommunity website and select  **CiviCRM Advanced Search**.
2. Once on the webpage select **"Organization"** under **Contact Type(s)** and the council you are working on under Group(s) e.g. Holdfast Bay Council then click Search.
3. Once on the search page select **All records**  and remember to select **EXPORT CONTACTS** and not delete contacts then click go.
4. On the fields page click on the **"Select fields for export"** and select **Subjects** mapping then proceed by clicking continue.
5. Recheck if the mapping (First four rows: Organization on the left column and Internal Contact ID, Organization Name, Organization...: Primary Category and Subjects: Subject_id on the right column) and then proceed by selecting Export.
6. Lastly open the csv file and then click on save as "Excel workbook" with the extension .xlsx and rename the file to follow the format  CouncilName_FinancialYr_CiviCRM.xlsx  e.g., Holdfast Bay_54_26_CiviCRM.xlsx.
___
## Extract data for Power BI report
1. Open prepared Python code (Council_Reports.ipynb) using VS code. This code file needs to be placed in the same folder of three raw data files (e.g., 25_26_GA4_All year.xlsx, Holdfast Bay Council_25_26_DataGov_export.xlsx, Holdfast Bay_54_26_CiviCRM.xlsx).
2. Run the python code to obtain the data for Power BI report. Change the name of the file to the format Power BI - Councel name_ FY_Landing Page.xlsx (e.g., Power BI - Holdfast Bay Council 2025-2026 Landing Page.xlsx).