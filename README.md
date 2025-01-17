# KrishiMitra: Chatbot with Intent Recognition

## Overview
KrishiMitra is an intelligent chatbot designed to assist farmers with their agricultural needs. Using advanced **Natural Language Processing (NLP)** and **Machine Learning**, it identifies user intents and provides relevant responses. The chatbot can help with tasks such as crop selection, pest control, irrigation guidance, weather updates, market rate inquiries, and government scheme information.

The chatbot is built using **Streamlit** to offer an interactive and user-friendly web interface tailored for farmers.

---

## Features
- **Intent Recognition**: Understands and categorizes user queries into predefined agricultural intents like crop advice, pest control, or market rates.
- **Dynamic Responses**: Provides accurate, context-aware responses to user inputs.
- **Conversation History**: Logs all interactions, which users can review later in the "Conversation History" tab.
- **Customizable Intents**: Update the `intents.json` file to extend functionality with new patterns and responses.
- **Interactive Web Interface**: Built with Streamlit for seamless interaction and ease of use.

---

## Technologies Used
- **Python**: The backbone of the application for NLP and data processing.
- **NLTK**: For preprocessing and tokenization of user inputs.
- **Scikit-learn**: Logistic Regression for machine learning-based intent classification.
- **Streamlit**: Provides an intuitive web interface for interacting with the chatbot.
- **JSON**: For defining chatbot intents and responses.
- **CSV**: Logs user-chatbot conversations for history tracking.

---

## Installation

### 1. Clone the Repository
```bash
git clone <repository-url>
cd <repository-directory>
```

### 2. Create a Virtual Environment (Optional but Recommended)
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

### 3. Install Required Packages
```bash
pip install -r requirements.txt
```

### 4. Download NLTK Data
```python
import nltk
nltk.download('punkt')
```

---

## Usage
To start the chatbot application, run:
```bash
streamlit run app.py
```

Once the application is running, interact with the chatbot via its web interface:
- Enter your query in the input box provided.
- Receive helpful responses based on your agricultural questions.
- Access past interactions through the "Conversation History" option.

---

## Intents Data
The chatbot's responses are determined by the `intents.json` file, which contains:
- **Tags**: Categories such as "crop_advice", "pest_control", and "market_rates".
- **Patterns**: Example user queries for each intent.
- **Responses**: Predefined replies based on the intent.

Sample structure of `intents.json`:
```json
[
  {
    "tag": "crop_advice",
    "patterns": ["What crops should I grow?", "Suggest crops for the season"],
    "responses": ["Based on the current season, you can grow rice or wheat. Ensure proper irrigation."]
  },
  {
    "tag": "market_rates",
    "patterns": ["What is the price of wheat today?", "Market rates for rice?"],
    "responses": ["Please check your local mandi for updated rates. Wheat is currently priced at ₹2000/quintal."]
  }
]
```

---

## Conversation History
All user-chatbot interactions are saved in a file named `chat_log.csv` with the following columns:
- **User Input**: The question or message entered by the user.
- **Chatbot Response**: The reply generated by KrishiMitra.
- **Timestamp**: The date and time of the interaction.

The conversation history can be reviewed by selecting the "Conversation History" option in the sidebar of the app.

---

## Future Enhancements
- **Regional Language Support**: Enable farmers to communicate in their native languages.
- **Voice Interaction**: Integrate speech-to-text and text-to-speech capabilities.
- **Real-Time Weather Updates**: Connect with weather APIs for instant updates.
- **Market Price Integration**: Provide live crop price data from government or local market APIs.
- **Advanced AI Models**: Enhance responses using deep learning techniques for more personalized advice.

---

## Contributing
Contributions to KrishiMitra are welcome! Feel free to open an issue or submit a pull request with your ideas for improving the chatbot's functionality.

---

## License
KrishiMitra is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments
- **NLTK** for enabling efficient text processing.
- **Scikit-learn** for robust intent classification using Logistic Regression.
- **Streamlit** for its simple yet powerful interface-building capabilities.
- **Farmers** for inspiring this project and providing real-world use cases.

---
