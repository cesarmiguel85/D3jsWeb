# SankeyWEB
A simple web site wrapper to display D3js graphs from Google Sheet data with a very basic zooming option control.
The goal is to integrate into datastudio or powerpoint using a WebPreview add-in.

For now only 2 graps:
* Collapsible tree graph
Format: ![Timeline example](/image_tree.jpg)
* Sankey graph
Format: ![Timeline example](/image_sankey.jpg)

## Technology
* HTML/CSS
* Import data from Google Sheet (do not forget to Publish to Web as tsv/csv)
* JQuery 2.1.4
* D3js for Graph generation




## COLLAPSIBLE TREE GRAPH
Format: ![Timeline example](/image_tree.jpg)

### GET input parameters
* key: google sheet key id 
* sheet: sheet's id (gid)
* rangenodes: range with data for nodes relationship (with headers, first line is ignored)
* (optional) width: width of element (px) - default view width
* (optional) height: height of element (px) - default view height
* (optional) zoom: scale factor  - default 1

### Data - Relationships table columns
* name: name of node
* parent: name of the parent node (use null for the source node)



** EXAMPLE REQUEST (ids are not real, link not working, it is just to give a syntax example) **

https://cesarmiguel85.github.io/D3jsWeb/tree.html?key=1RmLSPsRnB-s93FkFDrZnr5rGestwebNn0bQ1XbYYITc&sheet=1420769761&rangenodes=M1:O100&width=700&height=500&zoom=0.8



## SANKEY GRAPH
Format: ![Timeline example](/image_sankey.jpg)

### GET input parameters
* key: google sheet key id 
* sheet: sheet's id (gid)
* rangenodes: range with data for nodes (with headers, first line is ignored)
* rangelinks: range with data for links (with headers, first line is ignored)
* (optional) width: width of element (px) - default view width
* (optional) height: height of element (px) - default view height
* (optional) zoom: scale factor  - default 1

### Data
#### Nodes table (list of all nodes) columns
* id: node id (usually a number from 0 to n corresponding to position in vector/table)
* name: node name to be displayed
#### Links table (list of all links) columns
* source: position of source node (0 to n, can be the id if position used for id)
* target: position of target node (0 to n, can be the id if position used for id)
* value: weight of the link


** EXAMPLE REQUEST (ids are not real, link not working, it is just to give a syntax example) **

https://cesarmiguel85.github.io/D3jsWeb/sankey.html?key=1RmLSPsRnB-s93FkFDrZnr5rGestwebNn0bQ1XbYYITc&sheet=1420769761&rangenodes=E1:F50&rangelinks=M1:O100&width=700&height=500&zoom=0.8


