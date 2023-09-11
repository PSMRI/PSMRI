# AMRIT
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

A.M.R.I.T (Accessible Medical Records vis Integrated technology) is a digital health platform initially developed by Piramal Swasthya Management Research Institute (PSMRI). It connects beneficiaries, health facilities & the health workforce in an integrated ecosystem through technology. AMRIT is leveraged by multiple Health and Wellness centres across states in India with services such as 104 helpline, 1097 HIV helpline and telemedicine.

This repository maintains the documentation framework for AMRIT project. Built using [MkDocs](https://www.mkdocs.org/) and the static pages are written as markdown files.

# Prerequisite 
### [MkDocs](https://www.mkdocs.org/)
MkDocs is a fast, simple and downright gorgeous static site generator that's geared towards building project documentation. Documentation source files are written in Markdown, and configured with a single YAML configuration file.

This project uses Python. Please ensure that you have Python and pip installed. To install the Python packages listed in a `requirements.txt` file using pip, you can use the following command in your command prompt or terminal:

```
pip install -r requirements.txt
```

Alternatively, MkDocs can be installed with the following command:

```
pip install mkdocs
```
	  
Additionally swagger-ui-tag plug-in and material theme can be installed using the following commands:	

```
pip install mkdocs-swagger-ui-tag
pip install mkdocs-material
```
	  
MkDocs comes with a built-in development server that lets you preview your documentation as you work on it. Make sure you're in the same directory as the mkdocs.yml configuration file, and then start the server by running the mkdocs serve command.

```
mkdocs serve
```
  
Open up http://127.0.0.1:8000/ in your browser, and you'll see the documentation home page being displayed.

# **Modify the documentation**

- Clone this GitHub repository for which the content needs to be updated.    
  
- If you wish to update the API spec of a service, run the Spring code locally (`mvn spring-boot:run`) and load http://localhost:8080/v2/api-docs where 8080 is the default port and v2 is the version of the Swagger specification being used.  
    
- Copy the page content and save as `{module-name}-api-spec.json`. 

- Checkout the PSMRI module code from GitHub and save the above json file under `docs/api-specs/` folder.  
   
- Add `swagger-ui` tag in corresponding markdown file under `docs/api-reference` folder to include Swagger UI.  
   
- The markdown file path is mentioned in `mkdocs.yml` file under API-Reference navigation.    

- Execute mkdocs serve and load http://127.0.0.1:8000/ to view the updated content. 

# **Publish AMRIT website to GitHub pages**  

- Raise a merge request from `develop` branch to `main` branch.

- The workflow file `publish-site.yml` gets triggered once the merge is done.  

- The publishing status can be viewed under Actions tab 

  

  




