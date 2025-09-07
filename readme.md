Drafter: AI-Powered Document Editing Assistant

Overview
Drafter is an intelligent document editing assistant built with LangChain and powered by OpenAI's GPT-4o model. It enables users to interactively update and save text documents through a conversational interface. The application leverages a stateful agent architecture using LangGraph to manage document modifications and save operations, making it an efficient tool for collaborative writing or automated document drafting.
This project showcases proficiency in modern Python development, AI integration, and state machine design, making it an excellent addition to a portfolio for recruiters seeking candidates skilled in AI-driven applications and workflow automation.
Features

Interactive Document Editing: Update document content dynamically using the update tool.
File Saving: Save the document as a .txt file using the save tool.
Stateful Workflow: Maintains conversation history and document state using LangGraph's StateGraph.
Tool Integration: Seamlessly integrates with LangChain tools for structured interactions.
Error Handling: Robust handling of file operations and user inputs.
Extensible Design: Easily extendable to include additional tools or functionalities.

Technologies Used

Python 3.8+: Core programming language.
LangChain: Framework for building AI-driven applications with LLMs.
LangGraph: Manages stateful agent workflows.
OpenAI GPT-4o: Advanced language model for natural language processing.
python-dotenv: Environment variable management for secure API key handling.

Getting Started
Prerequisites

Python 3.8 or higher
OpenAI API key (set in a .env file)
Required Python packages:pip install langchain langchain-openai langgraph python-dotenv



Installation

Clone the repository:
git clone https://github.com/yourusername/drafter.git
cd drafter


Create and configure a .env file with your OpenAI API key:
OPENAI_API_KEY=your-api-key-here


Install dependencies:
pip install -r requirements.txt


Run the application:
python drafter.py



Usage

Start the Drafter application by running the script.
Interact with the assistant via the command line:
To update the document, provide new content (e.g., "Update the document with 'Hello, World!'").
To save the document, specify a filename (e.g., "Save the document as myfile").


The assistant will display the current document state after each update and confirm when the document is saved.
The process ends when the document is saved successfully.

Example interaction:
===== DRAFTER =====
USER: Update the document with 'This is a test document.'
AI: I'll update the document with the provided content.
USING TOOLS: ['update']
TOOL RESULT: Document has been updated successfully! The current content is:
This is a test document.

USER: Save the document as testfile
AI: I'll save the document as 'testfile.txt'.
USING TOOLS: ['save']
TOOL RESULT: Document has been saved successfully to 'testfile.txt'.

===== DRAFTER FINISHED =====

Project Structure

drafter.py: Main application script containing the agent logic, state management, and tool definitions.
.env: Stores environment variables (e.g., OpenAI API key).
README.md: This file, providing project documentation.

Why This Project Stands Out

AI-Driven Workflow: Demonstrates integration of advanced LLMs with structured tools for practical applications.
State Management: Utilizes LangGraph for robust, stateful conversation and document management.
Clean Code: Adheres to Python best practices with type hints, modular design, and clear documentation.
Scalability: Designed to be easily extended with additional tools or integrations.
Real-World Relevance: Applicable to document automation, collaborative writing, or AI-driven content management systems.

Contributing
Contributions are welcome! Please fork the repository, create a feature branch, and submit a pull request with your changes. Ensure your code follows PEP 8 guidelines and includes appropriate tests.
License
This project is licensed under the MIT License. See the LICENSE file for details.
Contact
For inquiries or feedback, please reach out via GitHub Issues.

Built with ❤️ by K C Darshan# Drafter-AI
