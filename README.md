# OmegleAI - My CS50 Final Project
Welcome to my final project in CS50! This project uses artificial intelligence to communicate with other people on [Omegle](https://www.omegle.com/), is almost fully automated, so just sit back and relax and watch the conversations unfold. It offers different type of AI personas as well as a custom made persona which user can modify to his own taste.

Video demo of the project can be accessed by clicking here!

# Features

The whole script was written in [Python 3.9.13](https://www.python.org/downloads/).
Modules used in Python were: 

 - selenium,
 - tkinter,
 - openai,
 - ttkthemes,
 as well as many others...
 This project relies on [OpenAI API Key](https://help.openai.com/en/articles/4936850-where-do-i-find-my-secret-api-key) usage which is needed to make this program run.
 It also uses [Chromium - WebDriver for Chrome.](https://chromedriver.chromium.org/downloads)

# Explaining the project

As stated before, the script uses artificial intelligence to communicate with other people on www.omegle.com. This project is almost fully automated(except for the setup part which is customizable thus the "almost" part). The script allows people to setup/customize their AI, or choose one of the already setup ones. It also features a user-friendly GUI windows which makes setting it up super easy to do!

## `OmegleAI.py`
Upon launching the script, user is greeted with a Setup window and easy-to-use settings. So let's go trought them together.
![Setup window](https://i.imgur.com/KqnZI7I.png)
**-Please input your API key from OpenAI**
	As the text says, it requires user to input his OpenAI API Key. The blue text is interactable and leads to a tutorial explaining how to obtain one. I should note that API Key from OpenAI is free, you just need to have an OpenAI account and you will be granted with free 5$ of credits! Don't worry, even though it may seem like a small amount, I can assure you it's going to last long! If you wish to know more about the AI prices, [click here.](https://openai.com/pricing)
	**DISCLAMER:** For this program to work you are going to need credits on your OpenAI account, simply opening one will grant you 5$ worth of credits. It's going to use some of those credits for AI usage.
	
**-Choose your AI**
	You can choose one of the already setup ones: Batman, Superman, Deadpool, or you can make your own AI by inputting your own prompt. Prompt that Batman uses goes like this:
	 "*The AI bot, embodying the persona of the enigmatic Batman, taps into the profound capabilities of the OpenAI Davinci language model. It possesses a remarkable level of awareness and intricacy, enabling it to discern and comprehend the historical context of previous messages exchanged. By leveraging the knowledge gained from previous interactions, which include the following messages from a stranger: "  `+  "\n".join(messages) +`  ", the bot assimilates a holistic understanding of the ongoing conversation. Now, in response to your latest message, which states: '"  `+  latest_message_text  +`  "', Batman's essence compels the bot to respond with utmost brevity, encapsulating his essence. Brace yourself for a concise yet potent response:*"
	 **PLEASE NOTE** The parts of the prompt that are highlighted are part of the code that are NOT going to work with the Custom AI, so you can just **skip them** and make a prompt without any code.
	 
**-Start chat**
Starts the program, which then turns on Chrome, but not your average Google Chrome, but Chromium, which is, as stated on their website "*...open source tool for automated testing of webapps across many browsers. It provides capabilities for navigating to web pages, user input, JavaScript execution, and more.*"

**-Close**
When you had enough, you can just press Close to stop everything and close everything. Clicking X on the top right does the same.
	

## Customizable options
Aside from Custom AI which we talked about, users can also customize their preferred topics. You can do that by opening the .py file and on 185th line :
![enter image description here](https://i.imgur.com/RceUbCf.png)

    topic  = ["batman", "comics", "meme", "talk", "music", "books"]
You can add/remove any topics you want, simply by using this format : `, "your topic"`.


## AI

AI always starts the chat by typing out "*hi there!*", which you can also change by changing the msg string on **61st and 210th** line.

Already set up AI models(Batman, Superman, Deadpool) have all the messages sent by other person saved in a list which is given to them every iteration. Custom AI sadly does **NOT** have that feature yet.

Every time it enters a new chat, the previous messages are deleted, so that AI forgets all about the last conversations and starts a new one.

The conversations are usually comical as you never know what he's going to say next, example:
![enter image description here](https://i.imgur.com/6k5v8Hx.png)
Everything typed here was typed by the AI.

The text is also stripped of interpunction signs and put in lowercase to look more "legit" like an internet user.
## Automatization

The topics are automatically inserted and it automatically starts searching for a chat, hence why the topics need to be changed in the code itself.
If the other person skips the chat, or perhaps even you, the program itself is going to start a new conversation.

## Requirements

 - **Python 3.9+ version**. Get it [here.](https://www.python.org/downloads/)
 - **Chromium Webdriver**. Your Chromium version **MUST** be the same version as your Google Chrome. Check your Chrome version by clicking at the 3 dots in the top right corner, then click Help > About Chrome. [Chromium download site.](https://chromedriver.chromium.org/downloads)
 - **OpenAI API Key** - already explained how to obtain one in OmegleAI.py section.
 - **Python modules:** 
	1.  `selenium`
	2. `tkinter`
	3.  `openai`
	4.  `ttkthemes`
	5.  `webdriver_manager (optional)`

# How to launch

 1.  Clone the code : 
 2. Install all required dependencies.
 3. Once installed run it with VSCode or via command prompt by running `python omegleai.py` when located in the OmegleAI folder.
 4. You are ready to go. **Enjoy!**






Want to know more about CS50? Head over [here!](https://pll.harvard.edu/course/cs50-introduction-computer-science?delta=0) 
