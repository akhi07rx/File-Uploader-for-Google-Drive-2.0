![maintenance-status](https://img.shields.io/badge/maintenance-actively--developed-brightgreen.svg)

# File Uploader for Google Drive 2.0

This project is a Python script that allows you to download files from a given URL and save them to a specified folder in your Google Drive. It supports a queue feature that allows you to add multiple download links to the queue and the script will automatically download them one by one. This can be useful when you need to download multiple files from different URLs and want to automate the process.

# Download files from URL to Google Drive with queue feature

## Project Description

This project is a Python script that allows you to download files from a given URL and save them to a specified folder in your Google Drive. It supports a queue feature that allows you to add multiple download links to the queue and the script will automatically download them one by one. This can be useful when you need to download multiple files from different URLs and want to automate the process.

## Features

- Download files from a given URL and save them to a specified folder in your Google Drive.
- Supports a queue feature that allows you to add multiple download links to the queue and the script will automatically download them one by one.
- Displays progress bar and information about the downloaded file, including file name, file size, total time, and saved location.

## Prerequisites

- This script is designed to run in Google Colab. Make sure you have a Google account and access to Google Colab.
- The script uses the following libraries: `tqdm`, `requests`, `google.colab`, `os`, `urllib.parse`, `os.path`, `sys`, and `time`. These libraries are pre-installed in Google Colab, so you don't need to install them manually.

## How to Use

1. Open Google Colab and create a new notebook.
2. Copy and paste the entire code into a single code cell in the notebook.
3. Run the code cell. The script will prompt you to authorize access to your Google Drive. Follow the instructions to authorize access.
4. Once access is authorized, the script will prompt you to enter a download link. Enter the download link and press enter.
5. The script will start downloading the file from the given URL and save it to the specified folder in your Google Drive.
6. While the file is being downloaded, you can keep adding more download links to the queue by entering them when prompted. The script will automatically download them one by one after the current download is completed.
7. To stop adding download links and exit the script, enter `exit` when prompted.

## Code Components

The code consists of several components:

- Importing necessary libraries: The script imports several libraries that are required for its operation, including `tqdm`, `requests`, `google.colab`, `os`, `urllib.parse`, `os.path`, `sys`, and `time`.
- Mounting Google Drive: The script uses the `google.colab` library to mount your Google Drive so that it can access and save files to it.
- Defining destination folder: The script defines a destination folder in your Google Drive where downloaded files will be saved. You can change this value to specify a different destination folder.
- Creating destination folder: The script checks if the destination folder exists and creates it if it doesn't exist.
- Defining download_file function: The script defines a `download_file` function that takes a URL as input and downloads the file from that URL. The function uses the `requests` library to send an HTTP GET request to the given URL and stream the response data. It also uses the `tqdm` library to display a progress bar while downloading the file. The function saves the downloaded file to the specified destination folder in your Google Drive.
- Initializing download queue: The script initializes an empty list that will be used as a queue for storing download links.
- Adding download links to queue: The script enters an infinite loop where it prompts the user to enter a download link or 'exit' to quit. If the user enters a download link, it is added to the queue. If the user enters 'exit', the loop is exited.
- Downloading files from queue: After exiting the loop, the script enters another loop where it pops URLs from the queue one by one and calls the `download_file` function to download each file.

## Acknowledgments

This code was developed with help from various online resources, including documentation for Python libraries such as `requests` and `tqdm`. We would like to thank all contributors who have shared their knowledge and expertise with us.

## License

This code is provided under an MIT license.
