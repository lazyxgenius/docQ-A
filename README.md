
# Document Q&A with FAISS, LangChain, and AWS Bedrock

This project demonstrates a Document Q&A system using FAISS for efficient document retrieval, integrated with LangChain for language processing, and models from AWS Bedrock. The system is set up to process PDF documents, embed their content using vector embeddings, and then allow users to query the documents for specific information. A Streamlit front end is provided for easy interaction.

## Project Structure

- **data1212/**: This folder contains two PDF documents generated by ChatGPT. These PDFs serve as the data source for the Q&A system.
- **faiss_index/**: This folder is generated by the code. It stores the FAISS index, which is used for efficient retrieval of document embeddings during the Q&A process.
- **req.txt**: This file lists all the required Python packages and dependencies for the project.

## Setup Instructions

### Installation

1. **Clone the Repository**

2. **Install Dependencies**

   Install the required Python packages listed in `req.txt`:

   ```bash
   pip install -r req.txt
   ```

3. **Set Up AWS Credentials**

   The project requires access to AWS services for the models. Set up your AWS account and configure the access key and secret key:

   ```bash
   aws configure
   ```

   During the configuration, you will be prompted to enter your AWS Access Key ID, Secret Access Key, region, and output format.

### Running the Project

1. **Start the Streamlit Front End**

   Once everything is set up, you can run the project with the Streamlit front end:

   ```bash
   streamlit run app.py
   ```

   This will start the Q&A system and open a web-based interface in your default browser.

2. **Interacting with the System**

   Through the Streamlit interface, you can upload documents, ask questions, and get answers based on the content of the PDF files. The FAISS index is used for efficient document retrieval, and AWS Bedrock models handle the language processing.

### Notes

- The FAISS index is automatically generated based on the documents in the `data1212` folder. If you add more documents, you may need to rebuild the FAISS index by rerunning the script.
- Ensure that your AWS credentials have the necessary permissions to access the services you intend to use.

