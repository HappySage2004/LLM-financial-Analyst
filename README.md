# LLM-financial-Analyst

### About :

### Libraries Used :
1. sec_edgar_downloader: to download the 10K filings
2. BeautifulSoup: to extract the text data from the XML format 10k filings. (HTML parsing)
3. Langchain: to make the pipelines for asking the questions to the Language Models and RAG. Also, the Hugging Face hosted models were accessed through the built-in langchain.llms HuggingFaceEndpoint() function.
4. Streamlit: To make the Graphics User Interface for the application.

### Further Improvements :
1. The insights from the LLMs were very generic and didn't provide precise and unique info. Possible cause was the output limit set by the HuggingFace Inference API endpoint. A possible solution would be to run the LLM locally using Quantized Weights.
2. The textual data provided to the LLMs in the form of embeddings was poorly formatted due to the vague format of the 10K filings downloaded from the SEC website. More specific preprocessing was not possible due to the variations of data locations in the filings of different companies.
