# File-Packer-Unpacker
Java-based file packing and unpacking utility that compresses multiple text files into a single file using custom headers and XOR-based encryption, and restores them back to original form with decryption.

## Project Overview
File Packer Unpacker is a Java-based utility application that combines multiple text files into a single packed file and later restores them back to their original form. The project also includes a basic XOR-based encryption and decryption mechanism for securing file contents during the packing process.

This project demonstrates:
- File Handling in Java
- Binary File Operations
- Encryption & Decryption
- Header Management
- Stream Handling
- Folder Traversal

---

# Features
- Packs multiple `.txt` files into a single file
- Unpacks packed files into original files
- XOR-based encryption for file security
- Automatic file extraction
- Header-based file metadata management
- Supports multiple text files
- Simple console-based interface

---

# Technologies Used
- Java
- File Handling
- FileInputStream
- FileOutputStream
- Byte Stream Operations
- XOR Encryption Technique

---

# Project Structure

```
FilePackerUnpacker/
│
├── program606.java
├── program614.java
└── README.md
```

---

# How It Works

## Packing Process
1. User enters folder name containing text files
2. Program scans all `.txt` files
3. Creates a packed file
4. Generates header containing:
   - File Name
   - File Size
5. Encrypts file data using XOR encryption
6. Stores encrypted data into packed file

---

## Unpacking Process
1. User enters packed file name
2. Program reads header information
3. Extracts:
   - Original File Name
   - File Size
4. Decrypts file data
5. Recreates original files

---

# Encryption Technique
The project uses a simple XOR encryption algorithm.

```java
Buffer[j] = (byte)(Buffer[j] ^ Key);
```

Key Used:

```java
0x11
```

The same key is used for:
- Encryption during packing
- Decryption during unpacking

---

# How to Run the Project

## Step 1: Compile the Programs

```
javac program606.java
javac program614.java
```

---

# Run Packing Program

```
java program606
```

Example Input:

```
Enter the name of folder :
Demo

Enter the name of packed file :
Packed.txt
```

---

# Run Unpacking Program

```
java program614
```

Example Input:

```
Enter the name of packed file :
Packed.txt
```

---

# Sample Output

## Packing

```
Folder is present
Number of files in the folder are : 5
```

---

## Unpacking

```
File Name : Notes.txt
File Size : 245
```

---

# Concepts Used
- File Handling
- Binary File Processing
- Header-Based Storage
- Encryption & Decryption
- Byte Stream Manipulation
- Dynamic Buffer Handling
- Directory Traversal

---

# Learning Outcomes
Through this project, you can learn:
- How file compression-like systems work
- How encryption and decryption operate
- Working with binary data in Java
- Managing multiple files programmatically
- Reading and writing byte streams
- Handling metadata using headers

---

# Future Enhancements
- GUI-based Application
- Support for all file formats
- Actual Compression Algorithms
- Password Protection
- AES Encryption
- Multi-folder Packing
- File Integrity Verification
- Progress Bar Implementation

---

# Author
Developed by Diksha Vispute as a File Handling and Encryption project using Java.
