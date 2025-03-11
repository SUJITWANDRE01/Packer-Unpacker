# Packer Unpacker

A Java application that provides functionality to pack multiple files into a single file and unpack a packed file back into its original form.

## Overview

Marvellous Packer Unpacker is a file handling utility designed to:
- **Pack** multiple files from a directory into a single file with custom headers
- **Unpack** previously packed files back to their original format
- Provide a simple and intuitive graphical interface for both operations

The application has built-in authentication and supports packing files with extensions `.txt`, `.c`, `.java`, and `.cpp`.

## Features

- **Secure Login System**: Authentication system with username and password validation
- **File Packing**: Pack multiple files from a specified directory into a single file
- **File Unpacking**: Extract all files from a packed file to their original form
- **User-Friendly Interface**: Simple GUI with clear instructions and feedback
- **File Filtering**: Selective packing based on file extensions
- **Error Handling**: Validation checks and error messages for smooth operation

## System Requirements

- Java Runtime Environment (JRE) 8 or higher
- Minimum 512MB RAM
- Windows/Linux/Mac OS

## Commands to Run the project

1. Compile the Java files:
   ```
   javac *.java
   ```

2. Run the application:
   ```
   java MarvellousMain
   ```

## Usage

### Login

1. Launch the application using `java MarvellousMain`
2. Enter username and password (default: MarvellousAdmin/MarvellousAdmin)
3. Username and password must be at least 8 characters long

### Packing Files

1. Click on "Pack Files" after logging in
2. Enter the source directory containing files to be packed
3. Enter the destination file name where you want to store the packed data
4. Click "SUBMIT" to pack the files

### Unpacking Files

1. Click on "Unpack Files" after logging in
2. Enter the name of the packed file you want to extract
3. Click "Extract Here" to unpack the files to the current directory

## Technical Details

### File Format

The packed file follows a specific format:
- Magic String: "Marvellous11" at the beginning of each packed file
- File Headers: Contains file name and size information (100 bytes)
- File Data: Actual contents of each file

### Classes and Their Functionality

- **MarvellousMain**: Entry point of the application
- **MarvellousLogin**: Handles user authentication
- **Template**: Base template for GUI components
- **NextPage**: Navigation page after successful login
- **MarvellousPackFront**: Front-end for packing operation
- **MarvellousPacker**: Back-end logic for packing files
- **MarvellousUnpackFront**: Front-end for unpacking operation
- **MarvellousUnpack**: Back-end logic for unpacking files


## Project Structure

```
├── MarvellousMain.java       # Main application entry
├── MarvellousLogin.java      # Login functionality
├── Template.java             # GUI template base class
├── NextPage.java             # Navigation after login
├── MarvellousPackFront.java  # Packing interface
├── MarvellousPacker.java     # Packing logic
├── MarvellousUnpackFront.java # Unpacking interface
├── MarvellousUnpack.java     # Unpacking logic
└── InvalidFileException.java # Custom exception
```

## Notes

- The packing operation only includes files with extensions `.txt`, `.c`, `.java`, and `.cpp`
- Default login credentials are "MarvellousAdmin" for both username and password
- After three failed login attempts, the application will exit
