# Nunaliit Schema Builder

A Drag-and-drop json builder for [nunaliit project](https://github.com/GCRC/nunaliit). This project can be easily extended to accommodate any project, which requires a GUI profile building tool. 

## Where can I see it in action?

It's hosted on github pages [here](https://qrafzv.github.io/json-builder/).

### Notes
* The project uses Backbone.js, Underscore.js, bootstrap.js, Requirejs, etc. 

* For development & debugging using the `index-dev.html` 
  
* Once done, change it back to build for production using the [r.js](https://github.com/jrburke/r.js/). 

* The full command is `r.js -o assets/js/lib/build.js` which should be run from the base directory.

* Then the program is deployed at `index.html`

### Adding new schema attribute

* In the js/data/ folder there is n2attributes.yaml files, each of which corresponds to a schema attribute in the schema builder.
* If you just want to add a new element you need to:
  - describe it in one of these files
  - parse the yaml to json using parse.rb in the same folder
  - create a corresponding template in the [templates/snippet directory]
  - add the template to [snippet-templates.js]
* If you want to add a new tab, you'll also need to adjust the [app.js file] to make sure the tab is loaded.

