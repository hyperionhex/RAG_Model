<!DOCTYPE html>
<html>
<body>

<h1>Business QA Retrieval Demo</h1>

<p>This repository contains a Google Colab notebook that demonstrates setting up a retrieval-based QA system to answer questions about B</p>

<h2>Overview</h2>

<p>The notebook does the following:</p>

<ol>
  <li>Loads the Wikipedia Simple Text Embedding dataset from Pinecone and preprocesses it</li>
  <li>Indexes the document embeddings into a Pinecone vector database</li> 
  <li>Defines an OpenAI text embedding model to embed question queries</li>
  <li>Creates a Pinecone vectorstore to interface the index and embeddings</li>
  <li>Defines a LangChain retrieval QA chain using ChatGPT, with the Pinecone vectorstore as the retriever</li>
  <li>Answers an example insurance question using the retrieval QA chain</li>  
</ol>

<h2>Requirements</h2>

<p>The notebook requires the following key libraries:</p>  

<ul>
  <li>LangChain v0.0.162</li>
  <li>OpenAI v0.27.7</li>
  <li>TikToken v0.4.0</li>
  <li>Pinecone Python SDK v2.2.1</li>
  <li>Pinecone Datasets v0.5.0rc10</li>  
</ul>

<p>To install requirements:</p>

<pre>
!pip install -qU \
  langchain==0.0.162 \
  openai==0.27.7 \
  tiktoken==0.4.0 \
  "pinecone-client[grpc]"==2.2.1 \
  pinecone_datasets=='0.5.0rc10' 
</pre>

<p>You will also need API keys for:</p>

<ul>
  <li>Pinecone</li>
  <li>OpenAI</li> 
</ul>

<h2>Usage</h2>

<p>To run the notebook:</p>

<ol>
  <li>Clone this repo</li>  
  <li>Open the notebook in Google Colab</li>
  <li>Run all cells - you will need to configure Pinecone and OpenAI keys</li>
  <li>Modify the example question and rerun as desired</li>  
</ol>

<p>The key components:</p>

<ul>
  <li><code>RetrievalQA</code> - LangChain QA chain</li>
  <li>Pinecone - Vector database</li>
  <li>OpenAI Embeddings - Text embedding model</li>  
</ul>

<h2>Customization</h2>

<p>The main ways to customize this:</p>

<ul>
  <li>Try different embedding models</li>
  <li>Change the dataset indexed into Pinecone</li> 
  <li>Modify the query questions</li>
  <li>Experiment with other LLMs than ChatGPT</li>
</ul>

<h2>Resources</h2>

<p>This demo uses:</p>

<ul>
  <li><a href="https://github.com/langchain-ai/langchain">LangChain</a></li>
  <li><a href="https://www.pinecone.io/">Pinecone</a></li>
  <li><a href="https://platform.openai.com/docs/overview">OpenAI Embeddings</a></li>  
</ul>

</body>
</html>
