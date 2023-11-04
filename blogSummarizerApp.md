---
layout: default
title: Blog Summarizer App
date: 2023-11-01
author: Garry Singh
categories: [OpenAI, Python, BeautifulSoap]
tags: [Python, OpenAI, Automation]
exclude: true
permalink: /AIinAction/blogSummarizerApp/
---
<head>

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
  <link rel="stylesheet" type="text/css" href="{{ '/assets/style/main.css' | relative_url }}">
   <link rel="stylesheet" type="text/css" href="{{ '/assets/style/aiInAction.css' | relative_url }}">
</head>

## <b>Blog Summarizer App</b> <span class="tag">[Github](https://github.com/codebygarrysingh/blog-summarizer-app/){:target="_blank"}</span>

The motivation behind creating a Blog Summarizer App is to showcase a common real-world implementation of <a href="https://en.wikipedia.org/wiki/Large_language_model" target="_blank">Large Language Models (LLM)</a> & <a href="https://en.wikipedia.org/wiki/Generative_artificial_intelligence" target="_blank">Generative AI</a>. Powered by Python and the OpenAI API, this app empowers content creators and bloggers to provide their readers with concise and coherent summaries, ensuring a smoother understanding of the main points.

<a href="https://codebygarrysingh.github.io/CElegansUnlocksTheSecretsOfSuperintelligence" target="_blank">See example summaries here</a>.
<br><br>
### <b>Key Features</b>
<hr class="custom-hr">
Blog summarizer is customizable app that let's users integrate generated summaries from their blog/article/content.

-- ***Automatic Summarization:*** Say goodbye to manual summarization. This app automates the process, saving you time and effort.

-- ***Customization:*** Tailor the summarization process to your specific needs. Adjust token limits and select the OpenAI model that suits your requirements.

-- ***Markdown Integration:*** Seamlessly process Markdown files and add summaries to specified insertion markers. Your blog articles will benefit from organized and compelling summaries.
<br><br>
### <b>Prerequisites</b>
<hr class="custom-hr">
Before using the Blog Summarizer App, ensure that you have the following prerequisites:

&nbsp;&nbsp;&nbsp;-- <a href="https://www.python.org/downloads/" target="_blank">Python 3.x</a> installed on your system.

&nbsp;&nbsp;&nbsp;-- An <a href="https://openai.com/blog/openai-api" target="_blank">OpenAI API key</a> for making API requests.
<br><br>
### <b>Installation</b>
<hr class="custom-hr">
Please follow below stepst to get started:

1. Clone the repository to your local machine:

```bash
# Use the following commands
git clone https://github.com/codebygarrysingh/blog-summarizer-app.git
cd blog-summarizer-app
```
2. Install the required Python packages using pip.

3. Configure your OpenAI API key in the config.py file:

<br>
### <b>Configurable Parameters</b>
<hr class="custom-hr">
You can customize the behavior of the Blog Summarizer App by modifying the constants and configurations in the config.py file. For example, you can change the OpenAI model, token limits, and insertion markers.

```markdown
	
# OpenAI API Key (Replace with your actual API key)
OPENAI_API_KEY = "YOUR_API_KEY_HERE"

# Directory containing Markdown blog articles
BLOG_DIR = "YOUR_BLOG_DIR_PATH_HERE"

# File extension for blog articles, for example .markdown
BLOG_FILE_EXT = "YOUR_BLOG_FILE_EXT_HERE"

# Offset for starting to read content from Markdown files
BLOG_OFFSET = 11

# Name of the OpenAI model to use for summarization
MODEL_NAME = "text-davinci-002"

# Maximum number of tokens for the response
MAX_RESPONSE_TOKENS = 150

# Insertion marker for the blog files
INSERTION_MARKER = "<!-- Insert Summary Here -->"

```
<br>

### <b>Navigating the code</b>
<hr class="custom-hr">
<br>
<b>Importing Necessary Libraries and Modules</b>

```Python
import os
import openai
import tiktoken
from bs4 import BeautifulSoup
import config
```
The code begins by importing several essential libraries and modules. Here’s what each of them does:

-- os: Allows interaction with the operating system, necessary for file operations.

-- openai: Provides access to OpenAI's GPT-3 model for text generation.

-- tiktoken: Helps count the number of tokens in a text string, useful for managing the model's limitations.

-- BeautifulSoup: Used for parsing and cleaning HTML content.

-- config: Imports configuration parameters from an external file.

<br>
<b>Constants and Configuration</b>
```Python
OPENAI_API_KEY = config.OPENAI_API_KEY
BLOG_DIR = config.BLOG_DIR
BLOG_FILE_EXT = config.BLOG_FILE_EXT
BLOG_OFFSET = config.BLOG_OFFSET
MODEL_NAME = config.MODEL_NAME
MAX_RESPONSE_TOKENS = config.MAX_RESPONSE_TOKENS
INSERTION_MARKER = config.INSERTION_MARKER
```
These constants and configurations are set up to store critical parameters like API keys, file paths, model names, and token limits.

<br>
<b>Initialize the OpenAI Client</b>
```Python
openai.api_key = OPENAI_API_KEY
```
The OpenAI API key is set to enable communication with OpenAI’s GPT-3 model.

<br>
<b>Token Counting Function</b>
```Python
def num_tokens_in_content(content: str, model_name: str) -> int:
    # ...
```
This function counts the number of tokens in a text string using the tiktoken library. It takes the content and the model name as input and returns the token count.

<br>
<b>Content Summarization Function</b>
```Python
def generate_blog_summary(content: str, model_name: str, max_tokens: int) -> str:
    # ...
```
This function generates a summary of the content using the OpenAI model. It takes the content, model name, and the maximum number of tokens for the generated summary as input. It returns the generated summary.

<br>
<b>Add Summary to Blog Function</b>
```Python
def add_summary_to_blogs():
    # ...
```
This function is responsible for processing and updating blog files with generated summaries. It iterates through files in the specified directory (BLOG_DIR). It processes only files with a specific file extension (BLOG_FILE_EXT). It reads the blog content, extracts the relevant text, generates a summary, and updates the blog file with the summary.

<br>
<b>Main Execution</b>
```Python
if __name__ == "__main__":
    add_summary_to_blogs()
```
The code checks if the script is being executed directly (not imported as a module) and then calls the add_summary_to_blogs() function to summarize the blog articles.

<br>
### <b>Usage</b>
<hr class="custom-hr">
The app will process the blog files, generate summaries, and update the content using the specified insertion markers. The summarized content will replace the marker in each file. Please follow steps below:

1. Place your blog articles in the designated directory
2. Configure the app using the constants in the config.py file. You can adjust token limits and other settings.
3. Run the app using the following command:
```shell
python main.py
```

<br>
### <b>Customization</b>
<hr class="custom-hr">
You can customize the behavior of the Blog Summarizer App by modifying the constants and configurations in the config.py file. For example, you can change the OpenAI model, token limits, and insertion markers.

<br>
### <b>License</b>
<hr class="custom-hr">
This project is licensed under the MIT License - see the LICENSE file for details.

<br>
### <b>Acknowledgements</b>
<hr class="custom-hr">
Special thanks to OpenAI for their powerful language models.
Inspired by the need to simplify the process of summarizing blog articles.

[Back to Showcase](/AIinAction/)
