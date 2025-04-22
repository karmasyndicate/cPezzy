# cPezzy - By Karma Syndicate

**Download URL:** https://t.me/+0z9FapS4mBgyZjhl

cPezzy is a powerful, user-friendly GUI tool designed by Karma Syndicate to validate cPanel credentials, filter credential lists, check SSH access, and upload files to valid cPanel accounts. This standalone .exe version packages everything into a single executable file, requiring no Python installation. The tool runs list filtering and displays results in an intuitive graphical interface, making it ideal for security researchers and administrators.

## Features

- **Credential Filtering**: Cleans and validates cPanel credential lists, removing duplicates and invalid formats, saving results to a new file.
- **cPanel Validation**: Checks the validity of cPanel credentials (e.g., `https://domain:2083|username|password`) using multi-threaded requests.
- **SSH Checking**: Optionally tests SSH access with provided credentials, supporting both root and user authentication.
- **File Uploading**: Uploads a specified file to validated cPanel accounts’ `public_html` directory.
- **Customizable Speed**: Adjust processing speed with a thread count slider (1-10).
- **Graphical Interface**: Modern GUI with a splash screen, progress bar, and detailed result display.

## Requirements

- Windows operating system (tested on Windows 10/11).
- No additional software or Python installation required; the `.exe` is fully standalone.

## How to Use

### 1. Prepare Your Credential File

Create a text file (e.g., `list.txt`) with cPanel credentials in the following format:

```
https://example.com:2083|user1|pass1
https://test.com:2083|user2|pass2
http://domain.com:2082:user3:pass3
invalid_line
```

- Each line should ideally follow `https://domain:2083|username|password`.
- The tool will silently filter out invalid entries and standardize formats (e.g., convert `http` to `https`, fix ports).

### 2. Download and Run the `.exe`

#### Obtain the Executable:
- Download `cpezzy.exe` from the provided source (e.g., a release link or shared folder).
- Place it in a directory of your choice (e.g., `C:\cPezzy`).

#### Run the `.exe`:
- Double-click `cpezzy.exe` or run it from the command line:

  ```sh
  C:\cPezzy\cPezzy.exe
  ```

### 3. Use the GUI

- **Splash Screen**: A brief splash screen appears on startup.
- **Select File**: Click "Browse" to load your `list.txt`.
- **Set Speed**: Adjust "Speed Boost" (1-10) for processing speed (default: 5).
- **Options**:
  - Check "Filter List" to clean the credential file.
  - Check "Crack SSH" and configure SSH options (root/user) in the popup.
  - Check "Upload File" and select a file to upload to valid cPanels.
- **Start**: Click "Start" to begin processing.
- **Results**: Validation progress and results (valid/invalid cPanel, SSH, uploads) appear in the GUI. Filtered lists and results are saved in a `cPanel_Result_X` folder next to the `.exe`.
- **Stop**: Click "Stop" to halt processing if needed.

## Output

- **Filtered File**: `cPanel_Result_X/Filtered cPanel - list.txt` (if "Filter List" is checked).
- **Validation Results**:
  - `Valid cPanel_X.txt`: Valid cPanel credentials.
  - `cPanel Main Domain_X.txt`: Valid main domain credentials.
  - `cPanel Not Working_X.txt`: Invalid credentials.
  - `SSH Found_X.txt`: Valid SSH credentials (if checked).
  - `Upload Success_X.txt`: Successful upload URLs (if checked).

![Alt text](https://raw.githubusercontent.com/karmasyndicate/poc/main/cpezzy.jpg)

## Notes

- **Portability**: The `.exe` is standalone and can be run on any Windows system without additional setup.

## Support

For issues or questions, contact Karma Syndicate via Telegram: https://t.me/KarmaSyndicate
https://t.me/xnabob
