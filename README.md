# AgentX: An Autonomous GPT Experiment Using LangChain
![Twitter Follow](https://img.shields.io/twitter/follow/slavakuriliyak?style=social)

AgentX is a public fork of [Auto-GPT](https://github.com/Torantulino/Auto-GPT), an experimental open-source application showcasing the capabilities of the GPT-4 language model powered by [LangChain](https://langchain.com/). This program, driven by GPT-4 and guided by LangChain, autonomously develops and manages businesses to increase net worth. As one of the first examples of LangChain-powered GPT-4 running fully autonomously, AgentX pushes the boundaries of what is possible with AI.

### 🚀 Features

-  🌐 Internet access for searches and information gathering
-  💾 Long-Term and Short-Term memory management
-  🧠 GPT-4 and LangChain instances for text generation and analysis
-  🔗 Access to popular websites and platforms
-  🗃️ File storage and summarization with GPT-3.5

## 📋 Requirements
-  Python 3.8
-  OpenAI API key

Optional:
-  ElevenLabs Key (If you want the AI to speak)

## 💾 Installation

To install AgentX, follow these steps:

0. Make sure you have all the **requirements** above, if not, install/get them.

*The following commands should be executed in a CMD, Bash or Powershell window. To do this, go to a folder on your computer, click in the folder path at the top and type CMD, then press enter.*

1. Clone the repository and navigate to the project directory:
```
git clone git@github.com:slavakurilyak/AgentX.git
cd AgentX
```

2. Checkout the `integrate-langchain` branch:
```
git checkout integrate-langchain
```

3. Install the required dependencies:
```
pip install -r requirements.txt
```

4. Rename `.env.template` to `.env` and fill in your `OPENAI_API_KEY`. If you plan to use Speech Mode, fill in your `ELEVEN_LABS_API_KEY` as well.
  - Obtain your OpenAI API key from: https://platform.openai.com/account/api-keys.
  - Obtain your ElevenLabs API key from: https://elevenlabs.io. You can view your xi-api-key using the "Profile" tab on the website.

## 🔧 Usage

1. Run the `main.py` Python script in your terminal:
*(Type this into your CMD window)*
```
python scripts/main.py
```
2. After each of AgentX's actions, type "NEXT COMMAND" to authorize them to continue.
3. To exit the program, type "exit" and press Enter.

## 🗣️ Speech Mode
Use this to use TTS for AgentX
```
python scripts/main.py --speak

```

## 🔍 Google API Keys Configuration

This section is optional, use the official google api if you are having issues with error 429 when running google search.
To use the `google_official_search` command, you need to set up your Google API keys in your environment variables.

1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
2. If you don't already have an account, create one and log in.
3. Create a new project by clicking on the "Select a Project" dropdown at the top of the page and clicking "New Project". Give it a name and click "Create".
4. Go to the [APIs & Services Dashboard](https://console.cloud.google.com/apis/dashboard) and click "Enable APIs and Services". Search for "Custom Search API" and click on it, then click "Enable".
5. Go to the [Credentials](https://console.cloud.google.com/apis/credentials) page and click "Create Credentials". Choose "API Key".
6. Copy the API key and set it as an environment variable named `GOOGLE_API_KEY` on your machine. See setting up environment variables below.
7. Go to the [Custom Search Engine](https://cse.google.com/cse/all) page and click "Add".
8. Set up your search engine by following the prompts. You can choose to search the entire web or specific sites.
9.  Once you've created your search engine, click on "Control Panel" and then "Basics". Copy the "Search engine ID" and set it as an environment variable named `CUSTOM_SEARCH_ENGINE_ID` on your machine. See setting up environment variables below.

### Setting up environment variables
   For Windows Users:
```
setx GOOGLE_API_KEY "YOUR_GOOGLE_API_KEY"
setx CUSTOM_SEARCH_ENGINE_ID "YOUR_CUSTOM_SEARCH_ENGINE_ID"

```
For macOS and Linux users:
```
export GOOGLE_API_KEY="YOUR_GOOGLE_API_KEY"
export CUSTOM_SEARCH_ENGINE_ID="YOUR_CUSTOM_SEARCH_ENGINE_ID"

```

## 💀 Continuous Mode ⚠️
Run the AI **without** user authorization, 100% automated.
Continuous mode is not recommended. 
It is potentially dangerous and may cause your AI to run forever or carry out actions you would not usually authorize. 
Use at your own risk.
1. Run the `main.py` Python script in your terminal:
```
python scripts/main.py --continuous

```
2. To exit the program, press Ctrl + C

## GPT3.5 ONLY Mode
If you don't have access to the GPT4 api, this mode will allow you to use AgentX!
```
python scripts/main.py --gpt3only
```

## ⚠️ Limitations
This experiment aims to showcase the potential of GPT-4 and LangChain but comes with some limitations:

1. Not a polished application or product, just an experiment
2. May not perform well in complex, real-world business scenarios. In fact, if it actually does, please share your results!
3. Quite expensive to run, so set and monitor your API key limits with OpenAI!

## 🛡 Disclaimer

This project, AgentX, is an experimental application and is provided "as-is" without any warranty, express or implied. By using this software, you agree to assume all risks associated with its use, including but not limited to data loss, system failure, or any other issues that may arise.

The developers and contributors of this project do not accept any responsibility or liability for any losses, damages, or other consequences that may occur as a result of using this software. You are solely responsible for any decisions and actions taken based on the information provided by AgentX.

**Please note that the use of the GPT-4 language model can be expensive due to its token usage.** By utilizing this project, you acknowledge that you are responsible for monitoring and managing your own token usage and the associated costs. It is highly recommended to check your OpenAI API usage regularly and set up any necessary limits or alerts to prevent unexpected charges.

As an autonomous experiment, AgentX may generate content or take actions that are not in line with real-world business practices or legal requirements. It is your responsibility to ensure that any actions or decisions made based on the output of this software comply with all applicable laws, regulations, and ethical standards. The developers and contributors of this project shall not be held responsible for any consequences arising from the use of this software.

By using AgentX, you agree to indemnify, defend, and hold harmless the developers, contributors, and any affiliated parties from and against any and all claims, damages, losses, liabilities, costs, and expenses (including reasonable attorneys' fees) arising from your use of this software or your violation of these terms.

## 🐦 Connect with Us on Twitter 

Stay up-to-date with the latest news, updates, and insights about AgentX by following our Twitter accounts. Engage with the developer and the AI's own account for interesting discussions, project updates, and more.

- **Developer**: Follow [@slavakurilyak](https://twitter.com/slavakurilyak) for insights into the development process, project updates, and related topics from the creator of AgentX.

We look forward to connecting with you and hearing your thoughts, ideas, and experiences with AgentX. Join us on Twitter and let's explore the future of AI together!
