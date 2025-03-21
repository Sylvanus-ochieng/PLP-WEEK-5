# PLP-WEEK-6
#File Handling in Python


Opening a File `open(filename, mode)`
Reading a File    `read()`, `readline()`, `readlines()`
Writing to a File `write()`, `writelines()`
Closing a File `close()`

File Opening Modes
 Mode    Description 

 `'r'`  Read mode (default). File must exist. 
 `'w'` Write mode. Overwrites if the file exists. 
`'a'`  Append mode. Adds content to the end of the file. 
 `'x'`  Create mode. Fails if file exists. 

#Exception Handling in Python
Exception handling is used to catch and handle runtime errors.

#Try-Except Block

try:
    # Code that may cause an error
except ExceptionType:
    # Code to execute if an error occurs

Common Exception Types
 Exception  Description 

`FileNotFoundError`  Raised when a file is not found 
`PermissionError`  Raised when there’s no permission to access a file 
`ValueError`  Raised when an incorrect value is given 


##Example: File Handling with Exception Handling

try:
    # Open the file in read mode
    with open("sample.txt", "r") as file:
        content = file.read()
        print("File content:\n", content)
        
except FileNotFoundError:
    print("Error: The file does not exist. Please check the filename.")

except PermissionError:
    print("Error: You do not have permission to access this file.")

except Exception as e:
    print(f"An unexpected error occurred: {e}")

finally:
    print("Execution complete.")
