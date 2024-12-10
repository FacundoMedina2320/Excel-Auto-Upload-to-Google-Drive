<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h1>Excel Auto Upload to Google Drive 📤</h1>
    <p>This project allows you to update an Excel file on Google Drive automatically from your PC using a Python script. Every time you execute the script, the latest version of your local Excel file will be uploaded or updated in Google Drive.</p>

<h2>Features ✨</h2>
    <ul>
        <li><strong>Automatic File Update</strong>: Sync your local Excel file with Google Drive each time you run the script.</li>
        <li><strong>Easy Integration</strong>: Simple Python script that works with Google Drive API.</li>
        <li><strong>Flexible</strong>: Customizable for your specific Google Drive folder and file name.</li>
        <li><strong>Cross-Platform</strong>: Works on both Windows and Linux.</li>
    </ul>

  <h2>Installation 🛠️</h2>
    <ol>
        <li><strong>Install Dependencies</strong>: Run the following command to install the required Python libraries:
            <pre><code>pip install google-api-python-client google-auth-httplib2 google-auth-oauthlib pandas openpyxl</code></pre>
        </li>
        <li><strong>Google API Setup</strong>:
            <ul>
                <li>Go to the <a href="https://console.developers.google.com/" target="_blank">Google Developer Console</a>.</li>
                <li>Create a new project.</li>
                <li>Enable the <strong>Google Drive API</strong> for the project.</li>
                <li>Set up <strong>OAuth 2.0 credentials</strong> and download the <code>credentials.json</code> file.</li>
                <li>Place the <code>credentials.json</code> file in your project directory.</li>
            </ul>
        </li>
    </ol>

  <h2>Script Overview 📋</h2>
    <p>This script will authenticate with Google Drive and either upload or update the specified Excel file in your Google Drive folder.</p>

  <h3>Code Explanation 🔍</h3>
    <ul>
        <li><strong>Authentication</strong>: The script authenticates via OAuth 2.0. When you run it for the first time, it will prompt you to log in and grant access to your Google Drive.</li>
        <li><strong>Upload/Update File</strong>: It checks whether the Excel file already exists on Google Drive. If it does, the script updates the file. If not, it uploads a new version.</li>
        <li><strong>Customization</strong>: 
            <ul>
                <li>Modify <code>local_file_path</code> to specify the path of your local Excel file.</li>
                <li>Set <code>google_drive_file_name</code> to the name you want the file to have on Google Drive.</li>
                <li>Replace <code>folder_id</code> with the Google Drive folder ID where you want to store the file.</li>
            </ul>
        </li>
    </ul>


   <h2>Running the Script 🚀</h2>
    <ol>
        <li>Save the script as a <code>.py</code> file.</li>
        <li>Open your terminal (or command prompt).</li>
        <li>Run the script:
            <pre><code>python your_script_name.py</code></pre>
        </li>
    </ol>
    <p>The script will automatically upload or update the specified Excel file in your Google Drive folder.</p>

   <h2>Automation ⏰</h2>
    <h3>Windows (Task Scheduler):</h3>
    <ul>
        <li>Open Task Scheduler.</li>
        <li>Create a new task with the desired trigger (e.g., daily, hourly).</li>
        <li>In "Actions", select "Start a Program" and point to the Python script.</li>
    </ul>

    <h3>Linux (Cron Job):</h3>
    <pre><code>
crontab -e
0 * * * * /usr/bin/python3 /path/to/your_script.py
    </code></pre>

   <h2>License 📄</h2>
    <p>This project is licensed under the <strong>MIT License</strong>. See the <a href="LICENSE">LICENSE</a> file for more details.</p>

   <h2>Contributing 🤝</h2>
    <p>Feel free to fork the repository, make improvements, and submit pull requests!</p>

   <h2>Acknowledgments 🌟</h2>
    <p>Special thanks to <a href="https://developers.google.com/drive" target="_blank">Google API Documentation</a> for the guide on integrating Google Drive with Python.</p>
</body>
</html>
