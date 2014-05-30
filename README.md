fontconversion
==============

Convert any font format or autohint it (ADFKO or ttfautohint) by command line or contextual menu in Finder.
Super easy.

#Command line usage

##Requirements
Fontforge

##Usage
	
	fontforge -script path/to/script.pe path/to/sourcefile
	
##Modification
If you want to change the way the fonts are converted, just read the FontForge script tutorial at http://fontforge.org/scripting-tutorial.html and do your own changes in .pe files.
	

#Services
##Requirements
OSX
AFDK and/or ttfautohint (if you want to use the autohint option)

##Install OSX Services
Copy *font-converter* folder to your user folder (/Users/yourusername/)
Copy files under *Services* folder to *~/Library/Services/* or double click to install them.

Services files execute this command:
	
	for f in "$@"
	do
		/usr/local/bin/fontforge -script ~/font-converter/script.pe "$f"
	done
	
You can change FontForge, scripts paths or parameters according to your needs.
Just double click services to open them in Automator.


##Usage
After copying services files to *Services* folder, 
*1. Open Finder
*2. Select your file
*3. Select Finder>Services menu. The different Services should be there. If not, restart Finder.
*4. Select your prefered conversion

# License

Copyright 2014 Andrés Torresi (@andrestorresi) - Huerta Tipográfica (@huertatipografica).

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0
See the License file included in this repository for further details.


