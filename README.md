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

QUESTION 2 EXPLANATION :

binary_to_text Function:

Takes a binary string as input.
Splits the binary string into 8-bit chunks.
Converts each 8-bit chunk from binary to decimal using std::bitset<8>.
Converts the decimal value to its ASCII character using static_cast<char>(byte.to_ulong()).
Appends the character to the final text.


QUESTION 3 EXPLANATION :

binary_to_text Function:

This function converts a binary string to its text equivalent. It processes the binary string in chunks of 8 bits, converts each chunk to a decimal value using std::bitset<8>, and then to an ASCII character using static_cast<char>(byte.to_ulong()).


read_file Function:

This function reads the entire content of a file into a string. It uses std::ifstream to open the file and std::istreambuf_iterator to read the contents.


find_flag Function:

This function searches for the flag pattern "IE_CTF{...}" in the decoded text. It locates the starting index of "IE_CTF{" and finds the corresponding closing brace "}". If both are found, it extracts and returns the flag.


main Function:

Sets the file path and calls the read_file, binary_to_text, and find_flag functions in sequence. It handles exceptions that might occur during file operations.

Example Usage:

The example binary string 0100100001100101011011000110110001101111 represents the text "Hello".
The function decodes this binary string to the text "Hello" and prints it.
