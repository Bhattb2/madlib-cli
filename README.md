# Madlib

## Description
- Print a welcome message to the user, explaining the Madlib process and command line interactions
- Read a template Madlib file (Example), and parse that file into usable parts.
- You need to decide what components of this file are useful, and how to break those useful pieces apart
- Once you know what parts of the template need user input, such as Adjective, prompt the user to submit a series of words to fit each of the required components of the Madlib template.
- With the collected user inputs, populate the template such that each provided input is placed into the correct position within the template.
- After the resulting Madlib has been completed, provide the completed response back to the user in the command line.
- Write the completed template (Example)to a new file on your file system (in the repo).

## Usage
The programs prompts the user to enter 21 different words. These words are appended to a list 'words'. The the function def open_template() opens the template.txt file and reads it. The system will loop through each character and if it will look for any words surrounded by the curly braces { }. It will then replace the word with a word from the words array. If the program encounters an error opening a file, it will create a new error_log file in the assests folder with a description of the error. See some code snipets below:

    with open(full_path, 'r') as original_template:
            contents = original_template.read()

    while not(last_word):
    for x in contents[:1]:
        if curly not in contents:
            last_word = True
        else: 
            a = contents.find('{')
            b = contents.find('}') 
            tobereplaced = contents[a:b+1]
            print(f'Please enter {tobereplaced[1:-1]}')
            word = input()
            words.append(word)
            value = words[count]
            new_content = contents.replace(tobereplaced, value, 1)
            contents = new_content

    with open('./assets/final_text.txt', 'w') as final_text:
    final_text.write(new_template)

## Challenges
- I spent a good amount of time attempting update the file because I was trying to update the existing template string. With assistance from a former classmate, I learned that strings are immutable. I resolved this by creating a new string.

## References
- https://www.pythonforbeginners.com/basics/string-manipulation-in-python
- https://www.youtube.com/watch?v=4mX0uPQFLDU
- https://realpython.com/read-write-files-python/
- https://thispointer.com/python-how-to-get-current-date-and-time-or-timestamp/

## Lab03 - Errors, Files, and Packaging


## Author
Bhagirath Bhatt