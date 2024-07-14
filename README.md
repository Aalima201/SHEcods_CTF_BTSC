QUESTION 1 EXPLANATION :
Atbash Cipher Function:

atbash_cipher: This function takes a string and returns its Atbash cipher equivalent. It iterates over each character, checking if it's an alphabet letter. If it is, it converts it to its counterpart in the reversed alphabet.


Repository Traversal:

find_flag_in_repository: This function traverses the given repository directory recursively, reading each .txt file. For each file, it decodes the content using the atbash_cipher function and searches for the flag format IE_CTF{...}.


Main Function:

Sets the path to the repository (repo_path) and calls find_flag_in_repository to find and print the flag along with the file path where it was found.

Usage

Set the Path: Update the repo_path variable in the main function to point to the repository's directory on your local system.

Compile and Run: Compile and run the C++ code.

