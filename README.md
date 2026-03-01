🔎 Inverted Search using Hashing & Linked Lists (C)

An efficient Inverted Search Engine implemented in C, built using core Data Structures concepts such as:

🔢 Hash Tables

🔗 Linked Lists

📂 File Handling

🧠 Dynamic Memory Allocation

This project simulates how search engines index data for fast retrieval.

📌 Project Overview

An Inverted Index maps:

Word  →  List of Files  →  Word Frequency

Instead of scanning every file during a search, the program:

Reads multiple text files

Uses hashing to organize words

Stores them in linked list structures

Allows efficient word searching

Time complexity for searching is improved using hashing techniques.

🧠 Data Structures Used
1️⃣ Hash Table

A fixed-size array (typically 26 indexes for alphabets)

Each index represents a bucket

Hash function determines the index using the first character of the word

index = tolower(word[0]) - 'a'

Each bucket stores a linked list of words.

2️⃣ Main Linked List (Word Node)

Each node contains:

Word

File count

Link to file list

Next word link (collision handling)

[ Word ] → [ Word ] → NULL

Used for handling collisions in hashing (Separate Chaining).

3️⃣ Sub Linked List (File Node)

For each word, a sub-linked list stores:

File name

Word count in that file

Next file link

Word
  ↓
[file1 | count] → [file2 | count] → NULL
🔥 Core Functionalities
✅ File Validation

Checks if file exists

Prevents duplicate files

Ensures proper file handling

✅ Create Database

Reads words from files

Applies hashing

Inserts into linked lists

Handles collisions using chaining

✅ Search Word

Computes hash index

Traverses word list

Displays file occurrences

✅ Display Database

Prints entire hash table

Shows words and file counts

✅ Save Database

Writes indexed structure to output file

✅ Update Database

Reloads saved database into memory

🗂️ Project Structure
main.c        → Program control
create.c      → Database creation (Hash + Linked List)
search.c      → Word searching logic
display.c     → Display entire database
save.c        → Save to file
update.c      → Update from saved file
validate.c    → File validation
header.h      → Structures & prototypes
⚙️ Compilation & Execution
Compile
gcc main.c create.c search.c display.c save.c update.c validate.c -o inverted_search
Run
./inverted_search file1.txt file2.txt file3.txt
📊 Example

If files contain:

file1.txt → hello hello world
file2.txt → hello data

The structure becomes:

Index[h]
  ↓
hello
  → file1.txt (2)
  → file2.txt (1)

Index[w]
  ↓
world
  → file1.txt (1)
🎯 Concepts Demonstrated

Hash Table Implementation

Collision Handling (Separate Chaining)

Singly Linked Lists

Nested Linked Lists

Dynamic Memory Allocation (malloc)

String Processing

File Handling in C

Modular Programming

📈 Time Complexity

Insertion: O(1) average

Search: O(1) average

Worst Case: O(n) (if many collisions)

👤 Author

MD ABDUL AZEEZ

📌 Educational Value

This project strengthens understanding of:

Real-world indexing systems

Search engine fundamentals

Efficient data organization

Core Data Structures implementation in C
