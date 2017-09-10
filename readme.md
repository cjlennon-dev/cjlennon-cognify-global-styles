# cjlennon-cognify-global-styles

LESS files and compiled CSS for cognify web application CSS styling

## Installation

- Clone the repo
- Compile the files in the `src/less` directory.

- running `npm run build` will run the 'build' script contained in `package.json`.  This script will comile the less folder using the `autoless` npm module (included as a dev dependency) and move the master css (`cjlennon-cognify-global-styles.css`) to the 'dist/css' folder.

Note that this script has been tested on Windows but may need modification for linux environments (uses the COPY command and escapes the slashes)

## Deployment

File `cjlennon-cognify-global-styles.css` contains all the css styling required.  Link to this file in your HTML page e.g. by hosting it yourself, uploading to a web server or using rawgit.com


