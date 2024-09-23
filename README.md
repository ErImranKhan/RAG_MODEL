<h1> 📄 Document Chat System </h1>
<hr>

This project is a Document Chat System that allows users to upload PDF documents, index them using Pinecone, and ask questions about the content of the documents. The system leverages Google's Generative AI models, Streamlit for the UI, Firebase for document metadata storage, and Pinecone for vector-based search.

<h2> 🚀 Features </h2> 

<p> PDF Upload: Users can upload PDF files which are parsed and indexed.</p>
<p> Document Indexing: The text from the PDF is split into manageable chunks and indexed into Pinecone for fast and efficient retrieval.</p>
<p> Question Answering: Users can ask questions related to the uploaded PDF documents. The system retrieves the relevant chunks and uses a generative AI model to generate the answers.</p>
<p> Validation: Basic validation on questions to ensure appropriateness.</p>
<p> Firebase Integration: Stores document index metadata in Firebase.</p>

<h2> 🛠️ Technologies Used </h2>

<p> Streamlit: For building the web UI.</p>
<p> PyPDF2: For reading and extracting text from PDF documents.</p>
<p> Langchain: For handling text splitting and conversational AI.</p>
<p> Google Generative AI: Used for embeddings and chat generation.</p>
<p> Pinecone: For vector-based document search.</p>
<p> Firebase: For storing metadata about document indices.</p>
<p> Python: Core language used for development.</p>

<h2> 📦 Installation </h2>

<p> 1. Clone the repository:
git clone https://github.com/your-username/document-chat-system.git
cd document-chat-system

2. Install the required dependencies: Create a virtual environment (optional but recommended) and install dependencies.
pip install -r requirements.txt

3. Set up environment variables: You can use a .env file to store sensitive API keys and credentials. Make sure to include the following in your .env:
GOOGLE_API_KEY=<Your Google API Key>
FIREBASE_API_KEY=<Your Firebase API Key>
PINECONE_API_KEY=<Your Pinecone API Key>

4. Initialize Firebase: Download the Firebase credentials file (.json) from your Firebase project and place it in the root folder. Update the filename in the code if needed:
os.environ["GOOGLE_APPLICATION_CREDENTIALS"] = "your-firebase-adminsdk.json"

5. Run the application: To start the Streamlit app, run:
streamlit run app.py </p>

<h2> 🔧 Configuration </h2>
<p> Pinecone Index: The code checks if the index exists in Pinecone and creates one if necessary. You can update the index name, dimension, and other settings in the Pinecone initialization section.</p>

<p> Firebase Firestore: Metadata regarding indexed documents is stored in Firestore for retrieval during question answering. Make sure you have the correct Firebase setup and credentials. </p>

<p> Generative AI: The AI model used for embeddings and QA is Google's Generative AI (Gemini-pro). Ensure you have appropriate access and API keys to use it.</p>

<h2> 📚 Usage </h2>

1. Uploading a PDF:

<p> Go to the Upload Document section. </p>
<p> Upload a PDF file and provide a unique Chat Name. </p>
<p> Click on the Upload and Index Document button to process and index the document.</p>

2. Asking Questions:
<p> Go to the Ask a Question section.</p>
<p> Enter the Chat Name of the previously uploaded document. </p>
<p> Ask a question related to the document content.</p>
<p> Click on the Submit Query button to receive an AI-generated response based on the document. </p>

<h2> 🛡️ Security </h2>
<p> Basic content validation is implemented to prevent offensive questions.</p>
<p> Ensure that your API keys and credentials are stored securely in your .env file or equivalent secret management systems. </p>

<h2> ⚠️ Limitations & Future Work </h2>

<p> The system currently supports only PDF documents. In the future, support for other formats (e.g., Word, HTML) can be added.</p>
<p> Basic validation for questions is implemented, but further improvements could include more sophisticated filtering. </p>
<p> The app currently uses a simple chunking method for text. In future iterations, more advanced NLP techniques could improve the chunking process. </p>

<h2> 🧑‍💻 Contributing </h2>
<p>If you'd like to contribute to this project, feel free to open a pull request or issue on the GitHub repository. All contributions are welcome!</p>

<h2> 📝 License </h2>
<p>This project is licensed under the MIT License. See the <c LICENSE> file for more details.</c>


