# evraz
Evraz Hackathon 3.0. Develop an application for automatic Code Review using AI.

Description:

1. Load and preprocess documents:
- load_and_preprocess_documents: Loads documents with company rules and standards, splits them into text chunks.
2. Create a vector store:
- create_vector_store: Creates a vector store using FAISS and OpenAIEmbeddings to store rules and standards.
3. Create a retrieval chain:
- create_retrieval_qa_chain: Creates a retrieval chain using RAG that will be used to check code for compliance with rules and standards.
4. Check code compliance:
- check_code_compliance: Uses a retrieval chain to check code for compliance with company rules and standards.
5. Run linters:
- run_linters: Runs linters (e.g. flake8, pylint) to automatically check code for syntax and style errors.
 6. Main code:
- main:
- Loads documents with rules and standards.
- Creates a vector store and a chain of search answers.
- Walks through the files in the project.
- Runs linters for each file.
- Checks the code for compliance with standards using RAG.
- Outputs the results of the check.

How to use:

1. Install libraries:

- pip install langchain openai faiss
2. Create files with rules and standards:

- Create text files company_standards.txt and coding_guidelines.md with company rules and standards.
3. Add API keys:

- Get the API key from OpenAI and add it to the ~/.env file (for example, OPENAI_API_KEY=your_key).
4. Replace /path/to/project:

- Replace this path with the path to the project you want to check.
 5. Run the code: 

- Run the main.py file.

Additional information:

- Configuring linters: 
- Configure linter commands (linter_commands) to check the code according to your standards.
- Extending functionality: 
- Add the ability to check different programming languages.
- Integrate the tool with version control systems (e.g. Git).
- Add the ability to automatically fix errors.

Important:

- Make sure you have access to the Internet, as the pipeline uses the OpenAI API.
- Make sure you have the necessary linters installed (e.g. flake8, pylint) and added the paths to them to linter_commands.
- Check the check results and configure the tool according to your requirements.
