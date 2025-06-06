# CU Boulder AED Inventory Work Planning System

A web-based application for planning AED (Automated External Defibrillator) inventory work at CU Boulder. This system helps organize student workers' routes across campus for maximum efficiency.

## 🎯 What This App Does

- **Creates Smart Routes**: Automatically groups nearby buildings into efficient work blocks
- **Interactive Maps**: Drag and drop buildings to customize routes
- **Time Calculations**: Estimates how long each building and route will take
- **Professional Reports**: Generates PDF work plans with maps and step-by-step instructions
- **Save Your Work**: Export and import your configurations

## 📱 Easy Setup Guide for Students

**Don't worry if you're not tech-savvy! These instructions will walk you through everything step-by-step.**

### What You'll Need
- A computer (Windows, Mac, or Linux)
- Internet connection
- About 10 minutes

---

## 🚀 Step-by-Step Instructions

### Step 1: Download Python (if you don't have it)

**What is Python?** It's a programming language that will run a simple web server on your computer.

#### For Windows:
1. Go to [python.org](https://python.org)
2. Click the big yellow "Download Python" button
3. Run the downloaded file
4. **IMPORTANT**: Check the box that says "Add Python to PATH" during installation
5. Click "Install Now" and wait for it to finish

#### For Mac:
1. Go to [python.org](https://python.org)
2. Click "Download Python for macOS"
3. Open the downloaded file and follow the installation steps

#### For Chromebook/Linux:
Python is usually already installed! Skip to Step 2.

---

### Step 2: Download This Project

#### Option A: Download as ZIP (Easiest)
1. Go to the GitHub page for this project
2. Look for a green "Code" button
3. Click it and select "Download ZIP"
4. Extract (unzip) the file to your Desktop
5. You should now have a folder on your Desktop

#### Option B: Using Git (if you know how)
```bash
git clone [GITHUB-URL-HERE]
```

---

### Step 3: Open Your Computer's Terminal

**What's a terminal?** It's a text-based way to give commands to your computer. Don't worry - we'll only use simple commands!

#### Windows Users:
1. Click the Start button
2. Type "Command Prompt" or "PowerShell"
3. Click on "Command Prompt" when it appears
4. A black window will open - this is your terminal!

#### Mac Users:
1. Press `Cmd + Space` to open Spotlight
2. Type "Terminal"
3. Press Enter
4. A window will open - this is your terminal!

#### Chromebook Users:
1. Press `Ctrl + Alt + T` to open the terminal
2. Type `shell` and press Enter

---

### Step 4: Navigate to Your Project Folder

In your terminal, you need to "go to" the folder where you downloaded the project.

#### If you put it on your Desktop:

**Windows:**
```
cd Desktop
cd "cu-boulder-aed-inventory-system"
```

**Mac:**
```
cd Desktop
cd "cu-boulder-aed-inventory-system"
```

**Tip**: If the folder has a different name, replace "cu-boulder-aed-inventory-system" with whatever your folder is actually called.

---

### Step 5: Start the Web Server

Copy and paste this command into your terminal and press Enter:

```
python -m http.server 8000
```

**If that doesn't work, try:**
```
python3 -m http.server 8000
```

**What you should see:**
The terminal will display something like:
```
Serving HTTP on :: port 8000 (http://[::]:8000/) ...
```

**🎉 Success!** Your web server is now running!

**Important**: Keep this terminal window open while using the app. If you close it, the app will stop working.

---

### Step 6: Open the App in Your Browser

1. Open your web browser (Chrome, Firefox, Safari, etc.)
2. In the address bar, type exactly: `http://localhost:8000/main.html`
3. Press Enter

**🎉 The app should now load!** You'll see a map of CU Boulder with building markers.

---

## 🎮 How to Use the App

### Basic Workflow:
1. **First time setup**: Click "Improve Building Locations" to get better GPS coordinates
2. **Create work blocks**: Click "Recalculate Clusters" to automatically group buildings
3. **Customize routes**: Drag buildings between groups or reorder them
4. **Generate reports**: Click "Generate PDF Report" to create printable work plans

### Key Features:
- **Drag the map pins**: Click and hold to move building locations
- **Drag buildings in lists**: Use the ⋮⋮ handle to reorder buildings
- **Edit building details**: Click "Edit" next to any building
- **Save your work**: Click "Save State to CSV" to backup your configuration

---

## 📄 Generating Work Reports

1. Make sure you have work blocks created (see "Recalculate Clusters")
2. Click "Generate PDF Report"
3. Wait a few moments for the PDF to generate
4. The report will automatically download to your computer
5. Print or share the PDF with your team!

---

## 🆘 Troubleshooting

### "Command not found" error:
- **Windows**: Make sure you checked "Add Python to PATH" during installation
- **Mac/Linux**: Try using `python3` instead of `python`

### App won't load in browser:
- Make sure the terminal is still running (you should see the "Serving HTTP" message)
- Check that you typed the address correctly: `http://localhost:8000/main.html`
- Try refreshing the page

### Maps not showing:
- Check your internet connection
- Try refreshing the page
- Some firewalls block map tiles - try from a different network

### PDF generation not working:
- Make sure you clicked "Recalculate Clusters" first
- Wait for all maps to fully load before generating PDF
- Try refreshing the page and trying again

### Still having problems?
- Close the terminal window
- Start over from Step 4
- Make sure you're in the right folder

---

## 🔄 Saving and Sharing Your Work

### To Save Your Configuration:
1. Click "Save State to CSV"
2. A file will download to your computer
3. Keep this file safe - it contains all your customizations!

### To Load a Previous Configuration:
1. Click "Load State from CSV"
2. Select the file you saved earlier
3. Everything will be restored exactly as you left it

### To Share with Others:
1. Save your state to CSV
2. Send the CSV file to your colleague
3. They can load it to see your exact setup

---

## 💡 Tips for Success

- **Start simple**: Generate clusters first, then customize
- **Save often**: Use "Save State to CSV" after making major changes
- **Test your routes**: Look at the generated maps to make sure they make sense
- **Print reports**: The PDF reports are designed to be printed and taken into the field
- **Ask for help**: If you get stuck, ask someone who's more tech-savvy to help with the setup

---

**Questions?** The terminal window will show any error messages. If something goes wrong, try closing everything and starting over from Step 4.

## 📋 Advanced Features (Optional)

*These features are for users who want to customize the system further:*

### Edit Global Variables
- Click "Edit Global Variables" to adjust timing assumptions
- Change walking speeds, AED inspection times, etc.
- Reset to defaults if needed

### Custom Building Settings
- Click "Edit" next to any building to modify details
- Adjust AED counts or search times for specific buildings
- Add building addresses for better PDF reports

### Travel Time Overrides
- Click "Edit" next to travel segments to set custom times
- Force walking or driving for specific routes
- Useful for buildings with special access requirements

---

## 📁 What's in This Project

When you download the project, you'll get:
- `main.html` - The complete application (this is the only file you need!)
- `README.md` - These instructions
- Some sample files showing what the system can generate

---

## 🏫 About This System

This tool was created to help CU Boulder organize AED inventory work efficiently. It:
- Groups nearby buildings to minimize travel time
- Estimates realistic time requirements for each task
- Generates professional reports for field teams
- Saves time and improves inventory accuracy

The system assumes each AED inspection takes about 5 minutes, plus time to locate devices in each building and travel between locations.

---

**Need Help?** 
- Try the troubleshooting section above
- Ask a tech-savvy friend to help with the initial setup
- The terminal window will show error messages if something goes wrong

**Questions about the AED inventory process itself?** 
Contact the CU Boulder Division of Public Safety.

---

*Last Updated: January 2025* 