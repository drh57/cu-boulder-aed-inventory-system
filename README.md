# 📋 **Complete Beginner's Guide: CU Boulder AED Inventory System**

## 🎯 **What This Program Does**
This is a web application that helps plan AED (Automated External Defibrillator) inventory work at CU Boulder by creating efficient routes, generating maps, calculating time estimates, and producing professional PDF reports for field teams.

---

## **📥 Step 1: Download the Program**

### **Easy Download Method (Recommended):**
1. Go to: **https://github.com/drh57/cu-boulder-aed-inventory-system**
2. Look for a green button that says **"Code"**
3. Click it and select **"Download ZIP"**
4. **Save the ZIP file to your Desktop**
5. **Right-click the ZIP file** and select **"Extract All"** (Windows) or **"Open"** (Mac)
6. You should now have a folder on your Desktop

### **Advanced Users (Git):**
```bash
git clone https://github.com/drh57/cu-boulder-aed-inventory-system.git
```

---

## **🐍 Step 2: Install Python (if you don't have it)**

### **Windows Users:**
1. Go to **python.org**
2. Click the big **"Download Python"** button
3. **Run the downloaded file**
4. **⚠️ CRITICAL**: Check the box that says **"Add Python to PATH"**
5. Click **"Install Now"**
6. Wait for installation to complete

### **Mac Users:**
1. Go to **python.org**
2. Click **"Download Python for macOS"**
3. Open the downloaded file and follow instructions

### **Test Python Installation:**
1. Open Terminal/Command Prompt (see next step)
2. Type: `python --version` and press Enter
3. You should see something like "Python 3.x.x"
4. If not, try: `python3 --version`

---

## **💻 Step 3: Open Your Terminal/Command Prompt**

### **Windows Users:**
1. Click the **Start button** (Windows logo)
2. Type: **"PowerShell"**
3. Click on **"Windows PowerShell"** when it appears
4. A blue window will open

### **Mac Users:**
1. Press **Cmd + Space** (Spotlight search)
2. Type: **"Terminal"**
3. Press **Enter**
4. A window will open

---

## **📁 Step 4: Navigate to Your Project Folder**

### **🎯 Super Easy Method (Recommended):**

#### **Windows:**
1. Open **File Explorer**
2. Find your downloaded project folder (probably on Desktop)
3. Hold **Shift** and **right-click** on the folder
4. Select **"Copy as path"**
5. In PowerShell, type: `cd ` (with a space after cd)
6. **Right-click** in PowerShell to paste the path
7. Press **Enter**

#### **Mac:**
1. Open **Finder**
2. Find your downloaded project folder (probably on Desktop)
3. Hold **Option** and **right-click** on the folder
4. Select **"Copy [folder name] as Pathname"**
5. In Terminal, type: `cd ` (with a space after cd)
6. Press **Cmd+V** to paste the path
7. Press **Enter**

### **Alternative Methods if Above Doesn't Work:**

#### **Method 1: Step-by-Step Navigation**

**Windows:**
```powershell
# Go to your user folder
cd ~
# Go to Desktop
cd Desktop
# List folders to see what's there
dir
# Go to project folder (use quotes for spaces!)
cd "cu-boulder-aed-inventory-system"
```

**Mac:**
```bash
# Go to your home folder
cd ~
# Go to Desktop
cd Desktop
# List folders to see what's there
ls
# Go to project folder
cd "cu-boulder-aed-inventory-system"
```

#### **Method 2: Direct Full Path**

**Windows:**
```powershell
cd "C:\Users\%USERNAME%\Desktop\cu-boulder-aed-inventory-system"
```

**Mac:**
```bash
cd "/Users/$USER/Desktop/cu-boulder-aed-inventory-system"
```

### **🔍 Verify You're in the Right Place:**
Type `dir` (Windows) or `ls` (Mac) and press Enter.

**You should see files like:**
- `main.html`
- `README.md`
- Various `.csv` files

---

## **🚀 Step 5: Start the Web Server**

Copy and paste this command into your terminal and press Enter:

```bash
python -m http.server 8000
```

**If that doesn't work, try:**
```bash
python3 -m http.server 8000
```

### **✅ Success Looks Like:**
You should see text like:
```
Serving HTTP on :: port 8000 (http://[::]:8000/) ...
```

**🔥 IMPORTANT:** 
- Keep this terminal window open! If you close it, the app stops working
- You might see some text appear when you use the app - this is normal
- Don't type anything else in this window while the server is running

---

## **🌐 Step 6: Open the App in Your Browser**

1. Open your web browser (Chrome, Firefox, Safari, Edge, etc.)
2. In the address bar, type **exactly**:
   ```
   http://localhost:8000/main.html
   ```
3. Press **Enter**

**🎉 Success!** You should see a map of CU Boulder with building markers and controls on the left side.

---

## **🎮 Step 7: How to Use the App**

### **First Time Setup (Do This Once):**
1. **Click "Improve Building Locations"** - This gets better GPS coordinates (wait for it to finish)
2. **Click "Recalculate Clusters"** - This groups buildings into efficient work blocks
3. You'll see buildings organized into different colored groups on the map

### **Basic Workflow:**
1. **Create work blocks**: Use "Recalculate Clusters" to automatically group nearby buildings
2. **Customize routes**: 
   - Drag buildings between groups in the left panel
   - Use the ⋮⋮ handle to reorder buildings within groups
   - Click and hold map pins to move building locations
3. **Generate reports**: Click "Generate PDF Report" to create printable work plans
4. **Save your work**: Click "Save State to CSV" to backup your configuration

### **Key Features:**
- **Interactive Map**: Click and drag the map pins to adjust building locations
- **Drag & Drop Lists**: Reorder buildings by dragging them in the left panel
- **Edit Buildings**: Click "Edit" next to any building to modify details
- **Time Estimates**: See estimated travel and work times for each route
- **Professional Reports**: Generate PDF reports with maps and instructions

---

## **📄 Generating Work Reports**

1. Make sure you have work blocks created (click "Recalculate Clusters" first)
2. Click **"Generate PDF Report"**
3. Wait a few moments for the PDF to generate (you'll see progress messages)
4. The report will automatically download to your computer
5. Print or share the PDF with your field team!

**The PDF includes:**
- Overview map with all routes
- Individual route maps
- Step-by-step instructions
- Time estimates for each building
- Total time calculations

---

## **🔄 Saving and Loading Your Work**

### **To Save Your Configuration:**
1. Click **"Save State to CSV"**
2. A file will download to your computer (usually to Downloads folder)
3. **Keep this file safe** - it contains all your customizations!

### **To Load a Previous Configuration:**
1. Click **"Load State from CSV"**
2. Select the file you saved earlier
3. Everything will be restored exactly as you left it

### **To Share with Colleagues:**
1. Save your state to CSV
2. Send the CSV file to your colleague
3. They can load it to see your exact setup

---

## **🆘 Troubleshooting Common Issues**

### **"Command not found" or "Python not recognized"**
- **Windows**: Reinstall Python and make sure you check "Add Python to PATH"
- **Mac**: Try using `python3` instead of `python`
- **Test**: Type `python --version` to verify installation

### **App won't load in browser**
- Make sure the terminal is still running (you should see "Serving HTTP" message)
- Check you typed the address correctly: `http://localhost:8000/main.html`
- Try refreshing the page (F5 or Ctrl+R)
- Make sure there are no typos in the URL

### **Terminal closed accidentally**
- Open terminal again
- Navigate to the folder (repeat Step 4)
- Start the server again (repeat Step 5)

### **Maps not showing**
- Check your internet connection (maps require internet)
- Try refreshing the page
- Some workplace firewalls block map tiles - try from a different network

### **PDF generation not working**
- Make sure you clicked "Recalculate Clusters" first
- Wait for all maps to fully load before generating PDF
- Try refreshing the page and trying again
- Check that you have buildings assigned to work blocks

### **"Access denied" or "Permission error"**
- Try running as administrator (Windows) or with `sudo` (Mac)
- Make sure the folder isn't in a restricted location
- Try moving the folder to your Desktop

### **Folder navigation problems**
- Use the path copying methods from Step 4
- Check for typos in folder names
- Use quotes around folder names with spaces
- Try using the drag-and-drop method

---

## **🔄 When You're Done Using the App**

### **To Stop the Program:**
1. Go back to your terminal window
2. Press **Ctrl + C** (this stops the server)
3. You can now close the terminal window

### **To Run the App Again Later:**
1. Open terminal/PowerShell
2. Navigate to the project folder (Step 4)
3. Start the server (Step 5)
4. Open browser to `http://localhost:8000/main.html` (Step 6)

**💡 Tip**: Bookmark `http://localhost:8000/main.html` for easy access when the server is running!

---

## **💡 Advanced Features (Optional)**

### **Customize Global Settings:**
- Click "Edit Global Variables" to adjust timing assumptions
- Change walking speeds, AED inspection times, etc.
- Reset to defaults if needed

### **Custom Building Settings:**
- Click "Edit" next to any building to modify details
- Adjust AED counts or search times for specific buildings
- Add building addresses for better PDF reports

### **Travel Time Overrides:**
- Click "Edit" next to travel segments to set custom times
- Force walking or driving for specific routes
- Useful for buildings with special access requirements

---

## **🎯 Pro Tips for Success**

1. **Start Simple**: Generate clusters first, then customize as needed
2. **Save Often**: Use "Save State to CSV" after making major changes
3. **Test Your Routes**: Look at the generated maps to make sure they make sense
4. **Print Reports**: The PDF reports are designed to be printed and taken into the field
5. **Internet Required**: You need internet for maps to display, but the app runs locally
6. **Keep Terminal Open**: The blue/black terminal window must stay open while using the app
7. **Bookmark the URL**: Save `http://localhost:8000/main.html` as a bookmark

---

## **🏫 About This System**

This tool was created to help CU Boulder organize AED inventory work efficiently. It:
- Groups nearby buildings to minimize travel time between locations
- Estimates realistic time requirements for each task
- Generates professional reports suitable for field teams
- Saves time and improves inventory accuracy
- Assumes each AED inspection takes about 5 minutes, plus building navigation time

The system helps student workers plan efficient routes across campus, reducing the time spent walking between distant buildings and ensuring comprehensive coverage of all AED locations.

---

## **📞 Still Need Help?**

### **Technical Issues:**
1. Check the troubleshooting section above
2. Ask a tech-savvy friend to help with the initial setup
3. The terminal window shows error messages if something goes wrong
4. Try starting over from Step 4 if things get confused

### **App Usage Questions:**
- Experiment with the different buttons to learn what they do
- The "Reset" options can help if you get stuck
- Save your work before trying major changes

### **AED Inventory Process Questions:**
Contact the CU Boulder Division of Public Safety for questions about the actual inventory procedures.

---

## **📋 Quick Reference**

### **Essential Commands:**
- **Windows Navigation**: `cd "C:\Users\%USERNAME%\Desktop\folder-name"`
- **Mac Navigation**: `cd "/Users/$USER/Desktop/folder-name"`
- **Start Server**: `python -m http.server 8000`
- **Stop Server**: Press `Ctrl + C` in terminal
- **App URL**: `http://localhost:8000/main.html`

### **File Locations:**
- **Downloaded files**: Usually in Downloads folder
- **Saved CSV files**: Usually in Downloads folder
- **Generated PDFs**: Usually in Downloads folder

---

**Questions?** The terminal window will show error messages if something goes wrong. Most issues can be solved by restarting from Step 4.

**Remember**: This runs locally on your computer - no data is sent to external servers, and you can use it offline once the maps are loaded!

---

*Last Updated: January 2025*
*Created for CU Boulder CUEMS AED Inventory Management*
