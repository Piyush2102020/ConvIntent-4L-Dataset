# ConvIntent-4L: Structured Chat Dataset with Tagged Intent and Emotion

**Description:**
ConvIntent-4L is an open-source dataset containing 400,000 formatted conversational samples designed to facilitate the training of conversational AI systems. Each sample is a single formatted string that incorporates context, user questions, bot responses, intent tags, and emotional cues. This structure is particularly suited for chatbots, open-domain dialogue systems, and models requiring enhanced understanding of conversation flow, user intent, and sentiment.

**Dataset Format:**
Each row in the dataset is a single formatted string based on a standardized structure. The dataset uses tokens to delineate conversation components such as context, user query, and bot response, making it easy to parse and use for model training. The format follows the structure outlined by the `build()` function.

**Format Details:**
Each entry has the following structure:

```
###cont### <context> ###user <intent>### <question> ###bot <emotion>### <response> ###end###
```

where:
- **###cont###**: Marks the start of the context provided for the conversation.
- **###user <intent>###**: Delimits the user input/question, with `<intent>` representing the user’s intent (e.g., informational, chatty).
- **###bot <emotion>###**: Introduces the bot’s response, with `<emotion>` indicating the emotional tone of the response (e.g., neutral, happy, sad).
- **###end###**: Marks the end of the conversation sample.

**Example Samples:**

Example 1:
```
###cont###architecturally, the school has a catholic character. atop the main building's gold dome is a golden statue of the virgin mary.###user informational###to whom did the virgin mary allegedly appear in 1858 in lourdes france?###bot neutral###saint bernadette soubirous.###end###
```

Example 2:
```
###cont###i often watch youtube videos about any interest.###user chatty###youtube is my wikipedia. videos about any interest.###bot neutral###i hadn’t thought about it that way.###end###
```

**Dataset Construction:**
The dataset was constructed using the `build()` function, which structures each conversation with:
- **Context**: Background text or setting relevant to the user’s question.
- **User Query**: The user's question or statement, labeled with an intent tag.
- **Bot Response**: The bot’s reply, labeled with an emotion tag.
- **Tokens**: Special tokens (`###cont###`, `###user <intent>###`, `###bot <emotion>###`, `###end###`) to mark conversation sections.

**Dataset Fields:**
- **Context**: Information or setup for the conversation.
- **User Intent**: Indicates the user's purpose or intent (e.g., neutral, happy, angry,sad ).
- **Bot Emotion**: The bot's emotional tone (e.g., neutral, happy, angry,sad).
- **End of Sample Token**: `###end###` token to mark the end of the formatted string.

**Use Cases:**
- **Conversational AI Training**: Ideal for open-domain chatbots or customer service models requiring nuanced context comprehension and response generation.
- **Sentiment and Intent Analysis**: Train models on emotion and intent-tagged data for sentiment and intent classification tasks.
- **Context-Aware Dialogue Modeling**: The formatted structure helps models understand conversation flow and context handling.

**Getting Started:**
1. **Download the Dataset:** [https://huggingface.co/datasets/piyush2102020/ConvIntent-4L/resolve/main/final_data_combined.csv]
2. **Data Loading and Parsing:** You can load each row as a single string and split on tokens (e.g., `###cont###`, `###user <intent>###`, etc.) to access each part of the conversation.
3. **Training Guidance:** For transformer-based models, consider tokenizing with special tokens corresponding to the format tags.

**Licensing:**
This dataset is provided under the MIT License.

**Contact Information:**
For questions or further inquiries, please reach out at bhattpiyush03@gmail.com.

---
