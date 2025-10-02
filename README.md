#PDF to XML n8n Workflow

This workflow automates the conversion of PDF invoices uploaded to a Google Drive folder into valid Cross-Industry Invoice (CII) XML files, adhering to the ISO 20022 standard. The process is fully automated and leverages AI for accurate data mapping and structured XML generation.

##Workflow Steps
The workflow is executed sequentially through the following nodes:

##Google Drive Trigger: 

Watches a specified Google Drive folder for new file uploads, initiating the process.

##Search Files and Folders: 

Confirms and retrieves the details of the newly uploaded file.

##Download File: 

Downloads the new PDF file from Google Drive into the workflow.

##Extract from File: 

Extracts the raw, structured data (text content, tables, etc.) from the PDF for further processing.

##Transform to XML (XML Node): 

Converts the extracted data into a basic, unstructured XML format.

##AI Agent: 

Uses an AI agent (backed by Google Gemini) to transform the unstructured XML into a fully compliant CII XML document, strictly following the ISO 20022 blueprint and mapping all extracted data fields accurately.

##Convert to File: 

Converts the AI-generated XML output (which is a text string) into a standard .xml file format for uploading.

##Upload File: 

Uploads the final, compliant CII XML file back to a specified Google Drive folder.
