# __AMRIT__
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

A.M.R.I.T (Accessible Medical Records vis Integrated technology) is a digital health platform initially developed by Piramal Swasthya Management Research Institute (PSMRI). It connects beneficiaries, health facilities & the health workforce in an integrated ecosystem through technology. AMRIT is leveraged by multiple Health and Wellness centres across states in India with services such as 104 helpline, 1097 HIV helpline and telemedicine.

This repository maintains the documentation framework for AMRIT project. Built using [MkDocs](https://www.mkdocs.org/) and the static pages are written as markdown files.

# [MkDocs](https://www.mkdocs.org/)
MkDocs is a fast, simple and downright gorgeous static site generator that's geared towards building project documentation. Documentation source files are written in Markdown, and configured with a single YAML configuration file.

Make sure the necessary pre-requisites like Python, MkDocs are installed to make any changes locally.MkDocs can be installed with the following command:  
**pip install mkdocs**    
	  
Additionally swagger-ui-tag plug-in and material theme can be installed using the following commands:	
** pip install mkdocs-swagger-ui-tag**    
** pip install mkdocs-material**    
	  
MkDocs comes with a built-in dev-server that lets you preview your documentation as you work on it. Make sure you're in the same directory as the mkdocs.yml configuration file, and then start the server by running the mkdocs serve command. 
  
Open up http://127.0.0.1:8000/ in your browser, and you'll see the default home page being displayed.    

# **Update AMRIT website content in Github pages**  

- Checkout the github module code for which the content needs to be updated.    
  
- Run the code locally and load http://localhost:8080/v2/api-docs where 8080 is the default port and v2 is the version of the Swagger specification being used.  
    
- Copy the page content and save as {module-name}-api-spec.json. 

- Checkout the PSMRI module code from github and save the above json file under docs/api-specs/ folder.  
   
- Add swagger-ui tag in corresponding markdown file under docs/api-reference folder to include Swagger UI.  
   
- The markdown file path is mentioned in mkdocs.yml file under API-Reference navigation.    

- Execute mkdocs serve and load http://127.0.0.1:8000/ to view the updated content. 






