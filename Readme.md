1. Generative AI      
The Generative AI make new content such as text, image, audio, etc based on pre-trained data     
- AI Diagram    
![image](https://github.com/khkwon01/LLM-AI/assets/8789421/8e1f830f-640e-4305-a52b-e8901f38bdd7)       
- The difference between common AI and Generative AI
![image](https://github.com/khkwon01/LLM-AI/assets/8789421/381f559c-785f-4b54-9ce3-3021e44bffbd)     

2. NLP history
- n-grams --> RNNs and LSTMs --> Transformers --> LLMs
  - n-grams: predict the next word based on previous word. (limited context and understanding)
  - RNNs and LSTMs: improved sequence learning (limited with processing large amounts of data)
  - Transformers: Efficiently identified relationships between words, enabled training on large datasets.
  - LLM: GPT(Generative pretrained transformer)

4. LLM = Transformer architecture + generate human language  (a type of text generative AI)
- Model size, Parameters, Tokens are very important
- LLM application examples : text classification, question answering, text generation, document summarization
![image](https://github.com/khkwon01/LLM-AI/assets/8789421/3d1ea84a-8c2a-405f-855f-389d637107dd)
- LLM lifecycle    
  <img width="809" alt="image" src="https://github.com/khkwon01/AI-LLM/assets/8789421/bc588393-a422-4894-8803-2d994c089cfc">     
- LLM essential items
  - Transformer : Cross-attention + Self-attention (parallel support) <--> recurrent architecture (sequential support)
    - encoder: identify valuable features from input text --> embedding: generate a meaningful representation of that text.
    - decoder: make an output using embedding resulting from encoder. (chatgpt only use this)
  - Prompt Engineering: provide input data for a better understanding of LLM    
  - Fine tuning: apply the specific data like text-classification based on pre-training data    

5. LLM Prediction Steps
- Receive prompt
  - ex> "Are you developing microservice-based applications?"
- Break input into tokens
  - ex> ["Are", "you", "developing", "microservice", "-", "based", "applications", "?"]
- Process tokens with Transformer architecture
  - Understand relationships between tokens and identify the all sentence meaning of this prompt
- Repeat the below steps until completing sentence.
  - Predict next token based on context
    - ex> {"I":0.6, "we":0.2, "you":0.1}
  - Select a word based on probability score
    - ex> "I"
