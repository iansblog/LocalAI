# LocalAI
The process of getting open source AI projects up and running on the windows ARM system, specifically “[Windows Dev Kit 2023](https://www.microsoft.com/en-gb/d/windows-dev-kit-2023/94K0P67W7581?activetab=pivot:overviewtab "Windows Dev Kit 2023")”.

While this is aimed at the MS Windows 11 desktop build of the "Windows Dev Kit 2023" we will be working mainly in the Windows Subsystem for Linux rather than Windows itself. This is due to issues with versions of Python and one of the foundational components Ollama does not have a Windows install at this time.  

----


In the root of the C Drive run the following GIT command, this will pull all files used in the examples and put them in the following directory, c:\LocalAI, if you change the location then you will need to update the examples to point to the correct location. 


git clone https://github.com/iansblog/LocalAI.git

----

- Step 1, Installing [Ollama](./1_Ollama/README.md)
- Step 2, Installing the [foundations](./2_Foundations/README.md) for privateGPT
- Step 3, Installing [privateGPT](./3_privateGPT_Primordial/README.md) (primordial version) & linking to the 1984 text document. 
- Step 4, Installing [privateGPT 2.x](./4_privateGPT2/README.md) & linking to the 1984 text document. 

----

## Running the diffrent versions of LocalAI after the install process. 

### tinydolphin
- Double click on the created shortcut.
- ollama run tinydolphin --verbose
- Why is the grass green?
- /bye
- exit

### llava for questions and image processing
-  Double click on the created shortcut. 
- ollama run llava --verbose
- Why is the grass green?
- Please describe what is in the image? /mnt/c/LocalAI/images/question.png
- /bye 
- exit

### privateGPT (primordial  version)
- Double click on the created shortcut. 
- cd /mnt/c/LocalAI/3_privateGPT_Primordial/
- conda activate LocalAI
- python privateGPT.py
- Who is Emmanuel Goldstein?
- ctrl + C 
- conda activate
- exit

### privateGPT (2.x)
- Double click on the created shortcut. 
- cd /mnt/c/LocalAI/4_privateGPT2
- conda activate LocalAI2
- poetry run python3.11 -m private_gpt
- Open a web browser and go to http://127.0.0.1:8001 

#### privateGPT (2.x) document ingestion
- Double click on the created shortcut. 
- cd /mnt/c/LocalAI/4_privateGPT2/privateGPT
- conda activate LocalAI2
- mkdir source_documents
- Copy your documents into the /mnt/c/LocalAI/4_privateGPT2/privateGPT/source_documents directory. 
- python ./scripts/ingest_folder.py /mnt/c/LocalAI/4_privateGPT2/privateGPT/source_documents
- poetry run python3.11 -m private_gpt

Supported documents include: 
- .csv: CSV
- .docx: Word Document
- .enex: EverNote
- .eml: Email
- .epub: EPub
- .html: HTML File
- .md: Markdown
- .msg: Outlook Message
- .odt: Open Document Text
- .pdf: Portable Document Format (PDF)
- .pptx : PowerPoint Document
- .txt: Text file (UTF-8)

For the latest supported files please view the [github](https://github.com/SamurAIGPT/EmbedAI?tab=readme-ov-file#data) page.


----
