# Installing Ollama
----

## Preparing the window's enviorement
  -  Turning on the following windows features. 
  	-  Virtual Machine Platform
  	-  Windows subsystem for Linux 

  -  Reboot

  -  Install Ubuntu from the MS store
  -  reboot
  -  Create a desktop shortcut, with this as the command: 
	  -  wsl --user root -d ubuntu

##  Using WSL to install Ollama.ai 
  -  Double click on the created shortcut. 
  -  curl -fsSL https://ollama.com/install.sh | sh

  -  After the install has finished 
	  -  ollama serve
      
      - Pull some of the LLMs
  		- ollama pull llava
  		- ollama pull mistral

----  

**Note:** *I have included the –-verbose option on the run commands, this is not needed but it is interesting to see the cost of each query, please remove it if you would prefer.*

## Test image processing with the llaval LLM
-  Double click on the created shortcut. 
- ollama run llava --verbose
- Please describe what is in the image? /mnt/c/LocalAI/images/question.png
- /bye 

## Test Local AI witht he mistral LLM
  -  Double click on the created shortcut. 
  - ollama run mistral --verbose
  - Why is the sky blue?
  - /bye 

## Pull other LLMs
  -  ollama pull tinyllama
  -  ollama pull tinydolphin
  -  ollama pull llama2
  -  ollama pull phi


## Test the tinydolphin LLM
  -  Double click on the created shortcut. 
  -  ollama run tinydolphin --verbose
  -  Why is grass green?
  -  /bye

## Other LLMs I like
  -  ollama pull tinyllama
  -  ollama pull llama2
  -  ollama pull phi

For a full list of supported LLMs please pop over to the following link. “[Supported ollama LLMs](https://ollama.com/library?sort=newest "Supported ollama LLMs")”

----

Return back to the main [README](./../README.md)


