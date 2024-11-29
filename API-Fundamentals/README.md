# 📱🔗 API Fundamentals </> Activity Instructions 🔗🌐 

## Required Software
1. Install any code editor of your choice for working with Python.
    - [Visual Studio Code](https://code.visualstudio.com) (Preferred)
    - [Sublime Text Editor](https://www.sublimetext.com)
    - [PyCharm](https://www.jetbrains.com/pycharm/)
2. Install [Python 3.12](https://www.python.org/downloads/release/python-3126/).
    - For Windows: Click [here](https://www.canva.com/design/DAGXNNZak2s/4VCE8Ecoh17LafDZ_bw1eg/edit?utm_content=DAGXNNZak2s&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton) for a     detailed Python installation or install using Microsoft Store. Verify installation by typing `python -V` in Windows PowerShell.
4. Install a software for testing API Endpoints:
    - [Bruno](https://www.usebruno.com) (Preferred)
    - [Postman](https://www.postman.com)
    - [Insomnia](https://insomnia.rest)
5. Install [Git Bash](https://git-scm.com/downloads).

## Setup working environment
- All sections assume that you are using the preferred software (Visual Studio Code and Bruno).
1. Open Git Bash and select (`cd {folder-name/directory-address}`) or create (`mkdir {folder-name}`) a folder you want to work this project on.
2. Clone the `API-Fundamentals` GitHub repository to the current folder by entering `git clone https://github.com/MachiBytes/API-Fundamentals.git`.
3. Open VS Code with the cloned repository by entering `code API-Fundamentals/` and install the "SQLite Explorer" extension.
4. Open a new terminal in VS Code by navigating to `Terminal` and select your preferred type (Powershell or Git Bash). 
5. Create a virtual environment with Python by entering `python -m venv venv` using the corresponding terminal of your OS (Windows - Powershell, MacOS/Linux - Terminal).
6. Activate the virtual environment using `./venv/Scripts/activate` (Windows) or `source venv/Scripts/activate` (MacOS/Linux).
    - For Windows: If you are receiving an error containing "cannot be loaded because running scripts is disabled on this system," enter `Set-ExecutionPolicy Unrestricted -Scope Process` first.
7. Install FastAPI module in Python using `pip install "fastapi[standard]"`.
    - Make sure to surround `fastapi[standard]` with double quotation marks to ensure that it works on your terminal.
8. Install Peewee module in Python using `pip install peewee`.

## CK PART
## END

## Part 5: Create a POST Endpoint for books

1. Enter the command `git stash` to temporarily save changes made but not commit to the main branch. This also allows you to pull the following files.
2. Pull the Part 5 files by entering `git pull origin part5`. Run the code by entering `fastapi dev main.py`.
3. Create or clone a Bruno Request. Change its name to "Store a Book", then change its method to POST and endpoint to `/books` using the same base URL.
4. Go to `Body`, add a JSON Body, and enter a JSON formatted entry with title and author for the book you want to create. Save and send the request.
   
![part5](https://github.com/user-attachments/assets/c885ed17-c865-4f09-80c5-4f8b8bca5359)

5. Verify and screenshot if the book is added in the "Get all books" Bruno request and the SQLite explorer table. 

## Part 6: Create a PUT Endpoint for books

1. Enter the command `git stash` and then pull the Part 6 files by entering `git pull origin part6`.
2. Run the code by entering `fastapi dev main.py`.
3. Create or clone a Bruno Request. Change its name to "Update a specific book", then change its method to PUT and endpoint to `/books/{book-id}` using the same base URL.
4. Go to `Body`, add a JSON Body, and enter a JSON formatted entry with title and author for the book you want to update.
5. Change `{book-id}` endpoint to the book id you want to update. Save and send the request. Notice the output when you enter a valid and invalid output.

![part6](https://github.com/user-attachments/assets/c90ee9ba-4005-4a49-9546-3f5ac8aaed5f)

6. Verify and screenshot if the book is updated in the "Get all books" Bruno request and the SQLite explorer table. 

## Part 7: Create a DELETE endpoint for books

1. Enter the command `git stash` and then pull the Part 7 files by entering `git pull origin part7`.
2. Run the code by entering `fastapi dev main.py`. 
3. Create or clone a Bruno Request. Change its name to "Delete a specific book", then change its method to DELETE and endpoint to `/books/{book-id}`.
4. Go to `Body` and if there is a `JSON` body, change it to `No Body`.
5. Change `{book-id}` endpoint to the book id you want to delete. Save and send the request.

![partr7](https://github.com/user-attachments/assets/3d5fce00-8bed-43c8-b252-6b48f1237b62)

6. Verify and screenshot if the book is deleted in the "Get all books" Bruno request and the SQLite explorer table. 

## Part 8: API Authentication

1. Enter the command `git stash` and then pull the Part 8 files by entering `git pull origin part8`.
2. Add `print(f"Request: {request}")` after line 11 in `main.py`. Run the code by entering `fastapi dev main.py`.

![part8-1](https://github.com/user-attachments/assets/92c860e9-cb36-47a5-a6b6-74a2f15f7fbd)

3. Attempt to run the Bruno "Get all books" request. Observe the output.
4. In Bruno, right-click the Collection, then go to `Settings` -> `Auth`, and change `No Auth` to `Bearer Token`.

![part8-2](https://github.com/user-attachments/assets/5b3ab64c-41ae-4724-afbf-d4f07440fca3)
![part8-3](https://github.com/user-attachments/assets/7aa78dee-cc4e-4383-99bf-10fc1810d5ad)

5. Copy `API_KEY` from `main.py` in VS code to the Token entry in Bruno and save.
6. Change Auth of each request from `No Auth` to `Inherit`.

![part8-4](https://github.com/user-attachments/assets/5724c5fe-1566-42aa-8fea-d8f56e6efee8)

7. Send the request and take a screenshot if the API returned a successful status (e.g. `202 Accepted`) and outputs correspondingly.

## Submission of Proofs

1. Compile all screenshot images in a drive folder.
2. Name each screenshot to its corresponding part with your surname (e.g. `SURNAME_PART1` or `SURNAME_PART1-a`).
3. Submit the drive folder link [here](https://forms.gle/fXqrcbWTwW5oraxYA).
