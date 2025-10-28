# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

# Date: 28.10.25
# Register no. 212223020011
# Aim: Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools

Stage 1 – Prompt for Code Generation

🗣️ Prompt Designed:

“Write a Python program that sends the same text input (‘Explain the importance of data privacy in AI systems’) to both OpenAI’s GPT API and Hugging Face’s text generation API. The script should print both responses separately for comparison.”

💻 AI-Generated Response:

import openai
from huggingface_hub import InferenceClient

# Initialize clients
openai.api_key = "YOUR_OPENAI_API_KEY"
hf_client = InferenceClient("HuggingFaceModelName", token="YOUR_HF_API_KEY")

# Input text
prompt = "Explain the importance of data privacy in AI systems"

# Get OpenAI response
openai_response = openai.ChatCompletion.create(
    model="gpt-4o-mini",
    messages=[{"role": "user", "content": prompt}]
)
openai_text = openai_response.choices[0].message.content

# Get Hugging Face response
hf_response = hf_client.text_generation(prompt, max_new_tokens=100)
hf_text = hf_response[0]['generated_text']

# Display both outputs
print("=== OpenAI Response ===")
print(openai_text)
print("\n=== Hugging Face Response ===")
print(hf_text)


🧩 AI Explanation:
This code connects to two AI platforms — OpenAI and Hugging Face.
It sends the same query to both APIs and prints their outputs, making it easier to compare tone, structure, and information style.

Stage 2 – Prompt for Output Comparison

🗣️ Prompt Designed:

“Compare the two AI-generated responses in terms of tone, factual accuracy, and level of detail. Present your findings in a concise table format.”

💬 AI-Generated Response:

Criteria	OpenAI Response	Hugging Face Response	Remarks
Tone	Professional and academic	Slightly informal	OpenAI uses more structured tone
Factual Accuracy	High, with emphasis on GDPR and ethics	Good, but lacks specific laws	OpenAI provides more specific facts
Level of Detail	In-depth with examples	Moderate detail	OpenAI gives more context

 AI Explanation:
OpenAI’s model provided a more comprehensive and precise explanation, while Hugging Face’s output was shorter and conversational. Both were factually correct but varied in depth.

Stage 3 – Prompt for Insight Generation

Prompt Designed:

“Based on the comparison, suggest which AI model would be more suitable for an academic project report on data ethics, and why. Also, recommend possible improvements for the less suitable model.”

AI-Generated Response:

OpenAI’s model would be more suitable for academic projects because it offers greater factual accuracy, consistent tone, and depth.
Hugging Face’s model, while easier to read, could be improved by adding references or structured arguments.
For future use, combining Hugging Face’s creativity with OpenAI’s analytical detail could produce balanced results.

Reflection Note (Sample – 180 words)

This activity helped me realize that writing clear and detailed prompts is more important than I thought. In the first prompt, I included specific instructions like “print both responses” and “same input,” which made the AI produce an organized code.
In the second prompt, I noticed that when I asked for a “concise table,” the AI automatically formatted the comparison neatly — showing how small wording changes can lead to big improvements.
Finally, the third prompt about insight generation made me appreciate how AI can provide reasoning beyond just coding — it can even suggest decision-making criteria.

If I were to refine my prompts, I’d include more technical parameters (like token limits or model names) in Stage 1 and maybe request visual charts for Stage 2.
Overall, I learned how to guide AI step by step to produce usable, insightful, and comparable results. 

Conclusion

This activity helped demonstrate how effective prompt design can turn AI tools into powerful coding assistants. By guiding AI to generate, compare, and interpret Python code, learners gained practical insight into integrating multiple AI systems. It reinforced that clear, structured prompts lead to accurate results and showed how AI can support both technical and analytical parts of a project.

Result: The corresponding Prompt is executed successfully.
