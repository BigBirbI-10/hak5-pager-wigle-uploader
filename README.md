# Hak5 Pineapple Pager - Wigle Uploader

This payload allows the **Hak5 WiFi Pineapple Pager** to upload collected wardriving data (CSV files) directly to [Wigle.net](https://wigle.net) using an internet connection. 

It automatically archives successfully uploaded files to prevent duplicates.

## Features
- Checks for Internet connection (Google DNS ping).
- Installs `curl` if missing.
- Iterates through the default Kismet/Wigle loot directory.
- Uploads files to Wigle API V2.
- Moves uploaded files to an `/uploaded` subdirectory upon success.
- Skips files that Wigle reports as "already uploaded."

## Prerequisites
1. A **Hak5 WiFi Pineapple Pager**.
2. A **Wigle.net** account.
3. Your Wigle API credentials (found at [Wigle.net Account Settings](https://wigle.net/account)).

## Installation

1. Connect the Pager to your computer via USB-C (Storage Mode).
2. Navigate to the payload directory:
   `/root/payloads/user/general/`
3. Create a new folder named `WigleUploader`.
4. Copy the `payload.sh` file from this repository into that folder.

## Configuration

**You must edit the script before use!**

1. Open `payload.sh` in a text editor (Notepad++, VS Code, etc).
2. Locate the Configuration section at the top:
   ```bash
   API_NAME="YOUR_API_NAME_HERE"
   API_TOKEN="YOUR_API_TOKEN_HERE"
