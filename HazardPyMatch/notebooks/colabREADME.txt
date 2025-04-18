We recommend you run HazardPyMatch_source.ipnyb in Google Colab.

This is the colab-specific ReadMe

HazardPyMatch is the a Chemical Inventory and Hazard Analysis Pipeline. 

This script prompts the user for Globally Harmonized System (GHS) H-codes. At least 1 H-code is required. See here for reference: https://pubchem.ncbi.nlm.nih.gov/ghs  

There are 2 types of file inputs. The first is a required Chemical Inventory or list stored as an .xlsx or .csv file. This file should have "Chemical_Inventory" in the file name and contain 2 required column names: "Chemical Name" and "CAS Number". Please view the code block at the top of the pipeline. Upload your chemical inventory to a Google Drive folder, making sure that the file path listed to the right of "source_folder" in the first code block of the pipeline code is correct. The second input is an optional folder containing PDF versions of laboratory protocols. Please store the protocols folder in the "source_folder" in your Google Drive ensuring that the name of the folder listed to the right of source_folder in the "protocols_folder" variable is correct.

We set "print_intermediate_steps" to false by default. Change to print_intermediate_steps = True if you want to print the chemical inventory at each step for debugging.

After uploading the chemical inventory, defining source_folder, protocols_folder, GHS H-codes and changing "print_intermediate_steps" if necessary, you can run the entire pipeline via the File menu at Runtime > Run all.

The inventory file is automatically loaded from your specified source folder, with missing CAS numbers populated using PubChem API. The pipeline retrieves GHS hazard classifications (H-codes), chemical name synonyms, and searches for protocol PDFs that mention these chemicals.

The final outputs include processed chemical inventory lists, matched protocol hazards, and visual analytics, all saved as Excel files and PNG charts in "source_folder" for further analysis.
