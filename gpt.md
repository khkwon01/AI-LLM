### 1. GPT Range
![image](https://github.com/khkwon01/AI-LLM/assets/8789421/8993e667-b7a7-478f-a993-229ffa1a8b60)

### 2. GPT History
| 연도 | 버전 및 설명 | 토큰 | 기타 |
|---|:---|---|---|
| `2017` | Attention is all you need 논문 출시 | |구글  | 
| `2018` | 첫번째 GPT 모델 소개 (117 백만 파라미터) | |  | 
| `2019` | GPT-2 모델 소개   (15억 파라미터)   | | | 
| `2020` | GPT-3 모델 소개   (1750억 파라미터) | |  | 
| `2022` | GPT-3.5 모델 소개 (1750억 파라미터) | 4096 | aka. ChatGPT  | 
| `2023` | GPT-4 모델 소개 (not open) | 8192 |  | 

### 3. GPT operation flow
- Prompt(user input) --> Model --> Completion (output) (* based on tokens)
  
### 4. GPT API Usage
- Install the openapi library
```
pip install openai
```
- Set your api key
```
export OPENAI_API_KEY="sk-xxx"
```
- Use openai in Python
```
import openai
```
- Call the chat endpoint
```
respose = openai.ChatCompletion.create(
        model="gpt-3.5-turbo",
        messages=[{"role": "user", "content": "you put data in here"}],
)
```
