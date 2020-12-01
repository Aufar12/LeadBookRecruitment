Web Scraping - MSIA Logistics
==========

This repository contains scripts to scrap the website of <a href='http://www.msialogistics.com/company/list'>MSIA Logistics</a>. The desired result should be json files and excel file.

Packages and Libraries
--------
- selenium,
- time,
- re,
- json,
- pandas

Tools
--------
- Python
- Jupyter Notebook (You can change the IDE based on your preference)
- Chrome Web Browser
- Chromedriver (You can download it here : https://chromedriver.chromium.org/ )
- Microsoft Excel (For storing values)
- Github 


Functions
--------
- scrapNormal (Scraps if the structure of the html is template 1*)
- differentScrap (Scraps if the structure of the html is template 2*)
- bonusPoint (Turning field and values to .xlsx file)
- questionOne (Turning field and values to company_index.json)
- questionTwo (Turning field and values to company_raw.json)
- questionOne (Turning field and values to company_parsed.json and contact_parsed.json)
- main (to Scrap for first selection of page to last selection of page)


Description of files
--------------------

filename                          |  description
----------------------------------|------------------------------------------------------------------------------------
Scrap MSIA Logistics.ipynb        |  The Scraping Code
company_index.json            	  |  Company Name, Company Link, Country
company_raw.json                  |  Company Name, Company Link, Company Address, Country, Company Phones, Company Fax, Company Emails, Company Website, Contacts, Company Industry
company_parsed.json               |  Company Name, Company Link, Company Address, Country, Company Phones, Company Fax, Company Website, Company Industry
contact_parsed.json               |  Company Name, Company Link, Country, Company Website, Contact Name, Contact Job Title, Contact Phone
bonusPoint.xlsx                   |  Both company_parsed and contact_parsed values combined.


How To Use
--------------------
1. <b>Installing Packages</b>
First, before using the program, the packages and libraries (as stated before) has to be installed. You can install it using the ‘pip install __libraryName__’ command on your terminal.

2. <b>Installing Chromedriver</b><br>
After installing the packages and libraries, you need to install chromedriver. Please note that you have to check your Chrome Browser version first.  You can do that by go to the settings on your Chrome and choose help. There you can see which version of Chrome you are using. Install the same chromedriver version as your current Chrome Web Browser.
 If you have installed the chromedriver, please put the chromdriver.exe in the same directory of the code. In Windows operation system, you can put the chromedriver in any directory but you have set it up in environment variable on the path section.

3. <b>Run the Code</b><br>
Run the code, and make sure you don’t miss all the functions in the code column (If you are using other than Jupyter Notebook, copy all the code into .py file and run the file). 


4. <b>Call the main() function</b><br>
The main() function has two parameter. The first scrap to page and the last page to scrap. For example if you call main(2, 24), it means you will scrap the web from page 2 until 24. In the documentation section, you can see that I call main(1,50) which means I’m scraping page 1 until 50.

5. <b>Result</b><br>
If the scraping process is finished, in your directory you will receive several json files and 1 excel file.   The json files are   company_index.json, company_raw.json, company_parsed.json and contact_parsed.json. The excel file is bonusPoint.xlsx.  
