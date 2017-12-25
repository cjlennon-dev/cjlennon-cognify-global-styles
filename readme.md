# cjlennon-cognify-global-styles


## Module overview

This module contains the styling for a number of components that are used in the cognify web application.  The source LESS files are included as well as the compiled css (`cognify-styles.css`)

Also included is `offcanvas.css` which adds small device support.


## Set up

### Pre-requisites

Styling contained in this module is designed to sit on top of AdminLTE https://github.com/almasaeed2010/AdminLTE (which itself sits on top of bootstrap).  



## Installation

### Local dev environment set up (optional)

1.  Clone the repo

2.  From the command line run `npm install`  This will install the `autoless` npm module which is required to build the LESS files

3.  From the command line run `npm run build`

    This will run the 'build' script contained in `package.json`.  This script will compile the less folder using the `autoless` npm module (included as a dev dependency) and move the master css (`cognify-styles.css`) to the 'dist/css' folder.

    Note that the `npm run build` script has been tested on Windows but may need modification for linux environments (uses the COPY command and escapes the slashes)

## Deployment

File `cognify-styles.css` contains all the css styling required.  Link to this file in your HTML page e.g. by hosting it yourself, uploading to a web server or using rawgit.com.  

You will need to include a reference to the AdminLTE css stylesheet before the reference to `cognify-styles.css`

For a quick start, include the following links in the `<head>` tag of your html.

````html
  <!-- Bootstrap 3.3.7 -->
      <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
    
      
      <!-- adminLTE styling -->
      <link rel="stylesheet" href="https://rawgit.com/cjlennon/AdminLTE/master/dist/css/AdminLTE.css">
     
      <!-- styles from the cjlennon-cognify-global-styles module -->
      <link rel="stylesheet" href="https://rawgit.com/cjlennon/cjlennon-cognify-global-styles/master/dist/css/cognify-styles.css">
    
      <!-- support off-canvas collapse -->
      <link rel="stylesheet" href="https://rawgit.com/cjlennon/cjlennon-cognify-global-styles/master/dist/css/offcanvas.css"> 
````
## More information (developers)

If you intend to extend or replace the `cjlennon-cognify-global-styles` styling with your own styling you may find the following information helpful

Each individual LESS file contains all the styling needed to style a component (e.g. the top navigation bar, the left menu, additional table styling etc).  These components are used accross the application.  In this way a consistant styling is achieved while still allowing modularisation of the application

The components will extend either an AdminLTE component (which itself may be extending a bootstrap component) or a bootstrap component.  As far as possible the components are designed to be able to be interchangable.  For example if you wanted to give your own styling to the top menu but retain all other cjlennon-cognify styling then you could omit the `top-nav.less` file from the build and expect the compiled css to correctly style all the other components contained in this repo.

The LESS files are either given their own name (e.g. `top-nav.less`) or named after the AdminLTE or bootstrap component they extend (e.g. `buttons.less`).   CSS classes are namded as `cjlennon-cognify-[component name]` where `[component name]` is the name of the component which is also the name of the LESS file