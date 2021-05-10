# SankeyWEB
A simple web site wrapper to display a Sankey Graph (horizontal weighted relationship graph).
Used to integrate a Sankey Graph into a Data Studio dashboard or Powerpoint (using WebPreview add-in).
Format: ![Timeline example](/image.jpg)

## Technology
* HTML/CSS
* JS manual parsing of TSV file
* Import data from Google Sheet (do not forget to Publish to Web as tsv)
* JQuery 2.1.4
* Google charts for Sankey Graph generation

## Input: GET parameters
* key: google sheet key id 
* sheet: sheet's id (gid)
* range: range with data (with headers, first line is ignored)
* width: width of element (px)
* height: height of element (px)

## Data
4 columns:
- From (text)
- To (text)
- Weight (number)
- Tooltip (text)

** EXAMPLE REQUEST (ids are not real, link not working, it is just to give a syntax example) **

https://cesarmiguel85.github.io/SankeyWEB/index.html?key=1RmLSPsRnB-s93FkFDrZnr5rGestwebNn0bQ1XbYYITc&sheet=1420769761&range=E2:G100&width=700&height=500
