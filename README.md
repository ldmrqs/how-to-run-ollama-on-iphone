# how to use ollama on your iphone

## requirements
- **ollama**
- **ngrok**
- **enchanted dev**

### 1. ollama:
* go to https://ollama.com/download do download ollama, choose which OS you’re currently using.
* once you’ve done downloading ollama, choose a model https://ollama.com/search
* after choosing a model, use the following command to download the model to your local machine: ```ollama pull glm-4.7-flash``` [glm-4.7-flash is just an illustration, choose whatever model you're comfortable with.]
* test if ollama is working by starting a chat with the model you selected > ```ollama run glm-4.7-flash```

if ollama is working, now let’s set ngrok.

### 2. ngrok:
_since i’m running ngrok on a macbook, i’ll be using mac’s terminal commands, you can select your OS by following ngrok’s documentation: https://ngrok.com/docs/getting-started_

* create an account on grok to get your auth-token
* go to terminal and run the command ```brew install ngrok```
* connect to your account ```ngrok config add-authtoken $YOUR_TOKEN``` 

**IMPORTANT:ollama’s default port is > _11434_**
* run the command ```ngrok http http://localhost:11434```

once this command is running, the terminal will be updated with ngrok showing that you’re online and the link to your web interface. 

copy the link on “Forwading”.

### 3. enchanted dev
* go to the app store and search for **“enchanted dev”**
* download “enchanted dev”
* open the “enchanted dev” app once it’s installed on your iphone
* it will ask you for an ollama api endpoint to connect to it
* go to settings > and paste the **“Forwading”** link you copied, or you can just type it.

# **403 ERROR**
if you’re running into a 403 error on ngrok, please just run the following command > ```ngrok http --host-header=rewrite localhost:11434```

## **OPEN WEBUI method**

now, if you prefer not use installed an app on your iPhone, you can use Open WebUI on your browser. 

follow the tutorial on this [video](https://youtu.be/syR0fT0rkgY?si=eGWZtuS7LbJ7mDRh) by Decoder, he explains it very well on how to run Open WebUI with ollama on using **Docker** and **Ngrok**.