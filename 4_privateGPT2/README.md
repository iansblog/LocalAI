# privateGPT 2.x

----

Double click on the created shortcut. 

Run the following:
- cd /mnt/c/LocalAI/4_privateGPT2
- conda create -n LocalAI2 python=3.11
- conda activate LocalAI2
- git clone https://github.com/imartinez/privateGPT && cd privateGPT && python3.11 -m venv .venv && source .venv/bin/activate && pip install --upgrade pip poetry && poetry install --with ui,local && ./scripts/setup 
- poetry run python3.11 -m private_gpt
- clear**NOTE:** This initial build can take some time, but the web site will load when it is done. 
- Open a web browser and go to http://127.0.0.1:8001 
- **NOTE:** This can take a moment watch the status information and when it is finished the site will load. 
- Ask the following question(s)
    - What is newspeak? 
    - Who is Julia?
    - Please list 3 examples of newspeak.    
- **NOTE:** This set of questions will yeald an error, this is expected, we have not ingested any content yet.  
-- CTRL +C to end the current session. 
- mkdir source_documents
- cp ./../../txt/*.txt ./source_documents/
- python ./scripts/ingest_folder.py /mnt/c/LocalAI/4_privateGPT2/privateGPT/source_documents
- **NOTE:** This may take a few moments.  
- poetry run python3.11 -m private_gpt
- Open a web browser and go to http://127.0.0.1:8001 
- Ask the following question(s)
    - What is newspeak? 
    - Who is Julia?
    - Please list 3 examples of newspeak.    

----

## Comments

- It is worth noting the improvement form the primordial version of privateGPT, it is now able to list 3 examples of newspeak rather then giving a response that is close to the what is newsspeak. 

----

### Notes

*Install commands*

The install commands have been taken from [docs.privategpt.dev](https://docs.privategpt.dev/overview/welcome/quickstart) the only change is to add the commands to a single line without the line breaks, if there are issues copy the commands directly from the offical documentation. 

*Chganging the settings & LLM model to use.*

To change the setting of the system look at the settings.yaml file, you can update hte LLM model and change other setting such as the port number the site is running on. 

----

Return back to the main [README](./../README.md)

----
