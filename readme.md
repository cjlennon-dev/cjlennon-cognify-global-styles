# cjlennon-cognify-global-styles

LESS files and compiled CSS for cognify web application CSS styling.

This styling is designed to sit on top of AdminLTE https://github.com/almasaeed2010/AdminLTE (which sits on top of bootstrap)

## Installation

- Clone the repo
- Compile the files in the `src/less` directory.

- running `npm run build` will run the 'build' script contained in `package.json`.  This script will compile the less folder using the `autoless` npm module (included as a dev dependency) and move the master css (`cognify-styles.css`) to the 'dist/css' folder.

Note that the `npm run build` script has been tested on Windows but may need modification for linux environments (uses the COPY command and escapes the slashes)

## Deployment

File `cognify-styles.css` contains all the css styling required.  Link to this file in your HTML page e.g. by hosting it yourself, uploading to a web server or using rawgit.com.  

You will need to include a reference to the AdminLTE css stylesheet before the reference to `cognify-styles.css`


