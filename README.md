# CU Boulder AED Inventory Work Planning System

A comprehensive web-based application for planning and optimizing AED (Automated External Defibrillator) inventory work at the University of Colorado Boulder campus.

## 🚀 Features

- **Interactive Campus Map**: Drag-and-drop building markers with real-time coordinate updates
- **Intelligent Clustering**: Automatically generates optimized work blocks based on time constraints
- **Manual Control**: Full drag-and-drop reordering of buildings within and between work blocks
- **Customizable Parameters**: Edit global variables like walking speeds, cluster times, and AED inspection times
- **Individual Building Settings**: Custom AED counts and search buffer times per building
- **Travel Time Editing**: Override automatic travel calculations with custom times
- **Progress Tracking**: Visual progress bar for geocoding operations
- **Professional PDF Reports**: Generate detailed work plans with maps and step-by-step instructions
- **State Management**: Save/load complete application state to CSV files
- **Building Management**: Edit, delete, and customize building information

## 📋 Requirements

- **Python 3.x** (for local web server)
- **Modern Web Browser** (Chrome, Firefox, Safari, Edge)
- **Internet Connection** (for map tiles and geocoding services)

## 🛠️ Setup Instructions

### Quick Start (5 minutes)

1. **Download the Project**
   ```bash
   git clone [YOUR-REPO-URL]
   cd "CUEMS AED Building Cluster Map and Time Calculation"
   ```

2. **Start the Local Server**
   ```bash
   python -m http.server 8000
   ```
   *Note: On some systems, you may need to use `python3` instead of `python`*

3. **Open in Browser**
   - Navigate to: `http://localhost:8000/main.html`
   - The application will load with CU Boulder building data

### Alternative Setup (if Python isn't available)

1. **Use any local web server** (XAMPP, WAMP, Live Server extension in VS Code, etc.)
2. **Or open directly** - Some browsers allow opening the HTML file directly, but map features may be limited

## 🎯 Quick Usage Guide

### Basic Workflow
1. **Initial Setup**: Use "Improve Building Locations" to get better GPS coordinates
2. **Configure Settings**: Click "Edit Global Variables" to customize timing parameters
3. **Generate Clusters**: Click "Recalculate Clusters" to create optimized work blocks
4. **Manual Adjustments**: Drag buildings between clusters or reorder within clusters
5. **Fine-tune Times**: Edit individual building AED counts and search buffer times
6. **Save Work**: Use "Save State to CSV" to preserve your configuration
7. **Generate Report**: Click "Generate PDF Report" for printable work plans

### Key Controls
- **Drag Pins**: Click and hold building markers to reposition them on the map
- **Drag Buildings**: Use the grip handle (⋮⋮) to reorder buildings in work blocks
- **Edit Buildings**: Click "Edit" next to any building to modify details
- **Edit Travel**: Click "Edit" next to travel segments to customize travel times
- **Delete Buildings**: Click "Delete" to remove buildings from work blocks

## 📁 File Structure

```
├── main.html                 # Main application file (contains everything)
├── README.md                 # This file
├── .gitignore                # Git ignore file
└── cu_boulder_aed_state.csv  # Saved state file (generated when you save)
```

## 💾 Data Management

### Saving Your Work
- Click **"Save State to CSV"** to export all settings, building data, and customizations
- File downloads as `cu_boulder_aed_state.csv`
- Move this file to your project directory for organization

### Loading Previous Work
- Click **"Load State from CSV"** to restore a previous session
- Select your saved CSV file
- All settings, custom coordinates, and arrangements will be restored

### What Gets Saved
- Global timing parameters
- Building coordinates (including manual adjustments)
- Custom AED counts and search buffer times
- Custom travel times between buildings
- Building addresses for PDF reports

## 🎛️ Configuration Options

### Global Variables (Edit Global Variables button)
- **Max Cluster Time**: Maximum minutes per work block (default: 240)
- **Available Workers**: Number of student workers (default: 10)
- **Time per AED**: Minutes to inspect each device (default: 5)
- **AED Search Buffer**: Default building search time (default: 8)
- **Walking/Driving Speeds**: Campus travel speeds
- **Travel Thresholds**: When to switch from walking to driving

### Per-Building Settings (Edit button next to each building)
- **AED Count**: Number of devices in this building
- **Search Buffer**: Custom time to locate AEDs in this building
- **Building Details**: Name, square footage, address

## 📊 Understanding the Output

### Work Blocks
Each work block shows:
- **Step Numbers**: Sequential order for visiting buildings
- **Travel Segments**: Time and method (walk/drive) between buildings
- **Building Times**: Total time including search, inventory, and navigation
- **Custom Indicators**: Asterisk (*) shows buildings with custom settings

### PDF Reports
Generated reports include:
- **Executive Summary**: Total time, buildings, and AEDs
- **Methodology**: Detailed explanation of time calculations
- **Step-by-Step Instructions**: Complete workflow for each work block
- **Route Maps**: Visual representation of each work block's path

## 🐛 Troubleshooting

### Common Issues

**Map not loading?**
- Check internet connection
- Ensure you're using `http://localhost:8000/main.html` (not file://)

**Buildings not appearing?**
- Click "Recalculate Clusters" to regenerate
- Check browser console for error messages

**Geocoding not working?**
- Check internet connection
- Try reducing the number of buildings if rate-limited

**PDF generation failing?**
- Ensure you have clusters generated first
- Check browser console for specific error messages

### Browser Compatibility
- **Chrome/Edge**: Full functionality
- **Firefox**: Full functionality
- **Safari**: Full functionality
- **Internet Explorer**: Not supported

## 🤝 Collaboration

### Sharing Configurations
1. Save your state to CSV
2. Share the CSV file with colleagues
3. They can load it to get your exact configuration

### Best Practices
- Save state after major changes
- Use descriptive filenames for different scenarios
- Keep backups of working configurations
- Document any custom changes in file names

## 📝 Technical Details

### Technologies Used
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Mapping**: Leaflet.js with OpenStreetMap tiles
- **PDF Generation**: jsPDF with html2canvas
- **Geocoding**: Nominatim (OpenStreetMap)
- **Server**: Python HTTP server (development)

### Data Sources
- Building coordinates: Manual geocoding and adjustments
- Campus layout: OpenStreetMap
- Building data: CU Boulder facilities information

## 📄 License

This project is for internal use at the University of Colorado Boulder. Please respect rate limits when using geocoding services.

## 👥 Support

For technical issues or questions:
1. Check the troubleshooting section above
2. Review browser console for error messages
3. Contact the development team with specific error details

---

**Last Updated**: January 2025  
**Version**: 1.0  
**Compatibility**: Modern web browsers with JavaScript enabled 