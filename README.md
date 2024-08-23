# Sharing HTML Files Locally on Your Home Network

## Step 1: Prepare Your Files

1. Create a folder to contain your HTML file(s) and any associated assets (CSS, JavaScript, images, etc.).
2. Place your HTML file(s) in this folder.

## Step 2: Find Your Computer's IP Address

- On Windows:
  1. Open Command Prompt
  2. Type `ipconfig` and press Enter
  3. Look for the "IPv4 Address" under your active network adapter

- On macOS or Linux:
  1. Open Terminal
  2. Type `ifconfig` (on some Linux systems, use `ip addr show` instead)
  3. Look for the "inet" address under your active network adapter

## Step 3: Start a Simple Python Web Server

1. Open a terminal or command prompt
2. Navigate to the folder containing your HTML file(s):
   ```
   cd path/to/your/folder
   ```
3. Start the Python web server:
   - For Python 3:
     ```
     python -m http.server 8000
     ```
   - For Python 2 (if you're using an older system):
     ```
     python -m SimpleHTTPServer 8000
     ```

## Step 4: Access Your HTML File

1. On the computer running the server, open a web browser and go to:
   ```
   http://localhost:8000
   ```

2. From other devices on your network, open a web browser and go to:
   ```
   http://[YOUR_IP_ADDRESS]:8000
   ```
   Replace `[YOUR_IP_ADDRESS]` with the IP address you found in Step 2.

3. If you have multiple HTML files, you'll see a directory listing. Click on the file you want to view.

## Step 5: Stopping the Server

- When you're done, go back to the terminal where the server is running and press `Ctrl+C` to stop it.

## Security Note

This method is suitable for temporary sharing on a trusted home network. It's not secure for long-term use or on public networks. Always be cautious about what files you share.
