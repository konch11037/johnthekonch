# Directories

1. .nuxt
	- Made each time a directory is changed
1. assets
	- un-compiled assets, like CSS and fonts
1. components
	- Vue.js components
	- No need to import the components into the .vue files.
1. layouts
	- Look and feel for the web app
1. Middleware
	- custom functions to be run when rendering the page
1. node modules
	- yup
1. pages
	- Application views and routes
1. plugins
	- yup again
1. static
	- The static directory is directly mapped to the server 
	root and contains files that have to keep their names 
	(e.g. robots.txt) or likely won't change (e.g. the favicon)
1. store
	- viewx store files
1. `nuxt.config.js`
	- single point of configuration for Nuxt. If you want to add modules or
	  overide settings, this is it. 
