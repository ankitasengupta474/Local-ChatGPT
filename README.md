# Local-ChatGPT
A fully offline ChatGPT-style AI chatbot using Ollama Docker (1B parameter model) and OpenWebUI, deployed for local use without internet. Runs on CPU with a downloaded dataset and utilizes nohup for persistent execution.

FEATURES :

  Offline AI Chatbot – No internet required after setup.
  Docker-Based Deployment – Uses Ollama and OpenWebUI.
  CPU-Friendly Execution – No need for a GPU.
  Persistent Background Execution – Uses nohup to run even after terminal closure.
  Web Interface – Easily accessible via OpenWebUI.

USE CASES:

Privacy-Focused AI Chatbot
Offline AI Experimentation
Developing and Testing Generative AI Applications

SETUP:-

 PREREQUISITES:
 
 - Ubuntu 20.04+ (or any recent version)
 - Basic terminal knowledge
 

 INSTALL DOCKER:
      
   sudo apt update && sudo apt upgrade -y
   sudo apt install -y docker.io
   sudo systemctl enable --now docker

  CHECK INSTALLATION:
   
   docker --version 

 INSTALL OLLAMA:

   curl -fsSL https://ollama.com/install.sh | sh

  START OLLAMA SERVICE:

   ollama serve  

  VERIFY INSTALLATION:

   ollama run llama2

 DOWNLOAD & LOAD THE AI MODEL(OLLAMA 1B PATAMETER MDEL:)

   ollama pull llama2:1b

  VERIFY MODEL WORK:

   ollama list
   ollama run llama2:1b

 DOWNLOAD AND RUN OPENWEBUI:

  PULL OPENWEBUI DOCKER IMAGE:

   docker pull ghcr.io/open-webui/open-webui:main

  RUN OPENWEBUI CONTAINER:

   docker run -d --name openwebui -p 3000:3000 -v openwebui-data:/app/data           ghcr.io/open-webui/open-webui:main

  RUN OPENWEBUI ON LOCALHOST:3000 OR LOCALHOST:8080 IN YOUR WEB BROWSER 

RUN EVERYTHING IN BACKGROUND:

 RUN IT WITHOUT TERMINAL:

  nohup /home/hp/openwebui_env/bin/ open-openwebui serve>openwebui.log 2>&1 &


  
  
     








 
