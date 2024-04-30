# Structured Data Capture
Within healthcare there are a plethora of forms and surveys which can collect significant amounts of patient data. Often times these forms are administered on paper, but have increasingly been digitized. Think of the last time you went to a doctor's appointment and were handed a tablet to complete several forms while in the waiting room. Also consider all the surveys you receive in your e-mail asking for your input. The structure and content of these forms will vary from practice to practice, limiting their interoperability, unless they are subsequently transformed and mapped to data standards. One way to improve the ability to exchange health information is through the [Structured Data Capture](https://hl7.org/fhir/uv/sdc/) principles described within the HL7 FHIR Implementation Guide.

# Repository Overview
This repository is focused on the development of a Python script which can extract FHIR (Fast Healthcare Interoperability Resources) from survey responses and subsequently pass this data to a Large Language Model (LLM), such as OpenAI's [GPT 3.5](https://platform.openai.com/docs/models/gpt-3-5-turbo) which powers [ChatGPT](https://chat.openai.com), to generate a patient narrative note. 

# Questionnaire Resource
Surveys, forms, or questionnaires (collectively referred to as questionnaires) are stored as a [Questionnaire Resource](https://hl7.org/fhir/r4/questionnaire.html). This resource contains the list of questions to be completed, as well as details for rendering within an application used to administer the questionnaire. The tool used for questionnaire creation in this repository is the [National Library of Medicine's Form Builder](https://formbuilder.nlm.nih.gov).

# QuestionnaireResponse Resource
A completed questionnaire is stored as a [QuestionnaireResponse Resource](https://hl7.org/fhir/r4/questionnaireresponse.html). This resource contains the answers to each question from the questionnaire, along with metadata describing the subject, date and method of completion, etc. The tool used for completion of surveys, which generates a QuestionnaireResponse is the [FHIR SDC SMART App](https://lhcforms.nlm.nih.gov/sdc).

# How to Use the Colab Notebook
* Navigate to [survey_extraction_and_llm_note_generator.ipynb](/survey_extraction_and_llm_note_generator.ipynb)

* Click button to open in Colab
  
  ![button to open in colab](/images/open_in_colab.png)

* Run cell to clone GitHub repo into Colab
  
  ![clone GitHub repo](/images/clone_repo.png)

* Run cell to install libraries and dependencies
  
  ![install libraries](/images/install_libraries.png)

* Run cell for questionnaire extraction
  
  ![questionnaire extraction](/images/questionnaire_extraction.png)

* Run cell to instantiate FHIR resources
  
  ![instantiate resources](/images/instantiate_fhir_resources.png)

* Run cell to prime function for call to LLM
  
  ![LLM](/images/llm_soap_note.png)

* Run helper functions

  ![helper functions](/images/helper_functions.png)

* Add OpenAI API key to access LLM

  ![secrets openai api key](/images/secrets_openai_api_key.png)

* Run main function and review output

  ![main function](/images/main_function.png)

  
