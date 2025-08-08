# Arabic-Recipe-Chatbot-with-Web-Scraping
This project combines web scraping and Retrieval-Augmented Generation (RAG) to build an intelligent Arabic cooking assistant chatbot.
It automatically scrapes recipes from Shamlola.com, extracts structured ingredients and instructions, and stores them in a searchable format.
The scraped content is then indexed and used to power a chatbot that can answer Arabic cooking questions using LangChain, ChromaDB, and the AraGPT2 language model.

 What It Does:
  - Scrapes Arabic recipes (title, ingredients, instructions) using Selenium + BeautifulSoup
     
  - Saves the scraped data into a clean recipes.txt file
     
  - Splits and indexes recipe data using LangChain and ChromaDB

  - Embeds text using sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2
    
  - Uses AraGPT2 (aubmindlab/aragpt2-medium) to generate responses in Arabic
    
  - Answers cooking-related questions like:
"ما طريقة عمل الكفتة؟"
"ما هي مكونات شوربة العدس؟"


Example Query:
  query = "طريقة عمل الكفتة؟"
  result = qa_chain.invoke({"question": query})
  print("🧠 الإجابة:", result["text"])


Tech Stack:

  - Selenium, BeautifulSoup, requests – for recipe scraping
  - LangChain, ChromaDB, sentence-transformers – for RAG system
  - AraGPT2 (aubmindlab/aragpt2-medium) – Arabic language generation
  - transformers, pipeline, HuggingFace – model orchestration

    
Output:
  - Recipes saved in a readable .txt format and used to build a semantic search chatbot capable of generating accurate cooking instructions in Arabic.
