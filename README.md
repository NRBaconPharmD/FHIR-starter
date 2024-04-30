# Structured Data Capture
Within healthcare there are a plethora of forms and surveys which can collect significant amounts of patient data. Often times these forms are administered on paper, but have increasingly been digitized. Think of the last time you went to a doctor's appointment and were handed a tablet to complete several forms while in the waiting room. Also consider all the surveys you receive in your e-mail asking for your input. The structure and content of these forms will vary from practice to practice, limiting their interoperability, unless they are subsequently transformed and mapped to data standards. 
https://hl7.org/fhir/uv/sdc/

# Repository Overview
This repository is focused on the development of a Python script which can extract FHIR (Fast Healthcare Interoperability Resources) from survey responses. An incomplete survey is stored as a FHIR Questionnaire resource and the completed surveys are stored as QuestionnaireResponse resources, both of which are coded in JSON.

# Questionnaire
Surveys, forms, or questionnaires (henceforth referred to as questionnaires) is stored as a [Questionnaire Resource](https://hl7.org/fhir/r4/questionnaire.html). This resource contains the list of questions to be completed, as well as details for rendering within an application used to administer the questionnaire. The tool used for questionnaire creation in this repository is the [National Library of Medicine's Form Builder](https://formbuilder.nlm.nih.gov).


# QuestionnaireResponse
A completed questionnaire is stored as a [QuestionnaireResponse Resource](https://hl7.org/fhir/r4/questionnaireresponse.html). This resource contains the answers to each question from the questionnaire, along with information about the patient, when, and how the questionnaire was completed. The tool used for completion of surveys, which generates a QuestionnaireResponse is the [FHIR SDC SMART App](https://lhcforms.nlm.nih.gov/sdc).
