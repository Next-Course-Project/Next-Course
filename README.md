# Next Course Registration Assistant
Welcome! Next Course is a Langflow-based AI assistant designed to help MS-HCI students at Georgia Tech seek out course information, recommendations, and reviews while planning their semester schedules. There is a tool-based and RAG-based version, and a Slack App is used to communicate with students.

The 'Next_Course_setup_and_sources.zip' file in this repository contains all the data files needed to run both versions, integrate the models with Slack, and utilize RAGAS for accuracy testing. 

For the complete setup and evaluation guide, please refer to 'Next Course Files and Components/Next CourseComplete Guide.docx' in the zip file.

## 1. Getting Started
To begin, create a Langflow account and download the [Langflow app](https://www.langflow.org/).
Next, download the zip file Next_Course_setup_and_sources and unzip it.

## 2. Uploading a Langflow model
Open the Langflow app and sign in. In the Projects panel in the top left corner, there is an upload icon titled 'Upload a Flow'. Click it and select either the RAG JSON file (Github Files/Langflow Files/RAG Assistant/Next Course RAG Assistant.json)
or the tool-based JSON file (Github Files/Langflow Files/Tool-based Assistant/Next Course Tool-Based Assistant.json).

**NOTE:** While the JSON files will set up the Langflow infrastructure for each model, you must create and enter your own API key for your selected agent. For the tool-based version, you must also provide the proper JSON path to the locally saved Catalogue, Course Review Excel Sheet, and MS-HCI Handbook files for each tool.

### Tool-Based setup
Once the tool-based file has been uploaded to Langflow, open it to view the model flow and enter the appropriate local data file path for each of the following tools: 
1. Catalogue Search - Spring 2026 Course Catalog.json
2. Course Review Search - Course Review Excel Sheet.json
3. MS-HCI Handbook - MS-HCI Handbook.json

Once the paths are updated, navigate to the Agent component and input the API key for the agent of your choice. Both versions currently use Anthropic Sonnet 4.5, but this can be easily changed in the Agent component.

### RAG setup
Once the RAG version has been uploaded to Langflow, open it to view the model flow and fill in the requirements for each component: 
1. Enter your OpenAI API key into the OpenAI Embeddings component
2. Enter your Astra DB application token into the Astra DB component
3. Enter the API key for your selected agent in the Agent component
