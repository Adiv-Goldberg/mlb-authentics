# MLB Authentication Hub

This repository contains front-end web tools to generate, organize, and display custom authentication certificates for baseball memorabilia. The project runs entirely in the browser using HTML, CSS, and JavaScript without requiring a backend server.

## Included Tools

### 1. [Certificate Generator](https://www.google.com/search?q=https://adiv-goldberg.github.io/mlb-authentics/mlb%2520authentics%2520maker.html)

This tool builds the actual PDF display documents.

* **Live Preview**: Type in item details (batter, pitcher, inning, pitch speed) and see the visual layout update instantly.
* **Auto-Numbering**: Generates a unique, repeatable Hologram ID based on the text inputs.
* **Custom Styling**: Includes numeric controls to tweak font sizes, text weights, and block alignment for every section of the page.
* **PDF Export**: Saves the certificate as a perfectly scaled 1-page PDF. The file names are created automatically using the item details.

### 2. [Archive Homepage](https://www.google.com/search?q=https://adiv-goldberg.github.io/mlb-authentics/)

This is the main viewing hub that acts as a database interface.

* **Google Sheets Integration**: Pulls live records directly from a public Google Sheet.
* **Search and Sort**: Filter the table instantly by Hologram ID or item info. Click the column headers to sort alphabetically or chronologically by date.
* **Smart QR Codes**: Click any Hologram ID in the table to create a QR code for that item's PDF. The tool uses a free API to shorten the URL in the background, keeping the QR code grid simple and easy to scan. You can download the code as a PNG.
* **Direct Linking**: Includes buttons to view the specific MLB highlight video for each item.

## How It Works Together (Personal Workflow)

*Note: This is a personal repository. Only I can upload new certificates to the database, but anyone is welcome to browse the archive.*

1. **Make a Certificate**: Open the generator tool, fill out the game details, and export the PDF.
2. **Host the File**: I upload that new PDF directly into this GitHub repository folder.
3. **Log the Item**: I add a new row to the connected Google Sheet, including the exact PDF file name, the Hologram ID, and any video links.
4. **View the Updates**: Refresh the homepage. The table will fetch the new row from Google Sheets and automatically create the correct viewing links and QR codes for visitors.

## Setup Requirements

* **Google Sheet Permissions**: The Google Sheet must be set to "General Access: Anyone with the link can view" for the homepage to read the data.
* **Sheet Formatting**: The homepage expects four columns in this order: Hologram ID, Item Information, PDF Name, and Play URL.
* **File Locations**: Generated PDFs are hosted in the same GitHub repository folder as the `index.html` file so the links map correctly.
