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
client = OpenAI()
respose = client.chat.completions.create(
    model="gpt-3.5-turbo",
    messages=msg
)

print(completion.choices[0].message.content)
```

### 5. Prompt Engineering
There are 3 types propmt engineering in OPENAI or Generative AI.
- one-shot learning
  - 관련 예제 없이 주어진 데이터를 예측하기 위해 prompt 입력 (추가적인 예제 데이터를 요구하지 않음)
  - Use case : simple tasks 예측
  - 가격 모델 : token당 비용 (input + output)
- few-shot learning
  - input 예제와 요구되는 output 데이터를 포함하여 prompt 입력 (추가적인 예제가 필요함)
  - Use case : 특별한 output를 가진 복잡한 tasks 예측
  - 가격 모델 : token당 비용 (input + output), long prompt가 발생 가능
  - https://github.com/f/awesome-chatgpt-prompts
- Prompt engineering tricks
  - context, role, tasks, trick(단계적 응답 요청)를 포함하여 detailed한 prompt 입력
  - Use case : Creative, complex tasks
  - 가격 모델 : token당 비용 (input + output), long prompt가 발생 가능
- fine-tuning
  - 특정 도메인 또는 데이터셋 기반으로 training 된 모델에 prompt 입력
  - Use case : Highly complex tasks
  - 가격 모델 : 기존 모델과 비교해 보면 fine-tuned 모델은 token당 몇십배 더 비쌈

![image](https://github.com/khkwon01/AI-LLM/assets/8789421/84f7bc93-4d47-4c6d-8851-3702b602d087)

