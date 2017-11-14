# Node
- Node is the JS engine outside the browser.
- npm is a Node package manager that lets you download and manage code packages other coders have written which you want to use in your project.

### Points to cover:
- ```package.json``` file holds metadata relevant to your project, including information about packages your project depends (i.e., your "dependencies").
- ```npm init``` to create package.json file. Hit ```Return``` several times afterward to skip ahead and say OK to the setup questions. Alternatively, instead of typing ```npm init```, type ```npm init -y``` to skip those questions.
- ```npm install package-name``` to install the package by name. This makes the package appear under the "dependencies" property in the ```package.json``` file.
- At this point, make sure you have a file called ```.gitignore``` (no extension) in your project and that you write ```node_modules``` on a new line inside that file. If the file is not there, create it and type ```node_modules``` inside. This will ensure Git ignores the node_modules folder and does not push it to GitHub. It is bad practice to put this folder (which can be very large) on GitHub. 
- ```npm install``` will look in the ```package.json``` file to see what dependencies are required by the project and will proceed to download them. Even though you use ```.gitignore``` to prevent ```node_modules``` from being pushed to GitHub, your ```package.json``` file is NOT ignored and IS pushed to GitHub, so when other coders clone your project, the ```package.json``` will be downloaded along with the project. They can then run ```npm install``` in their command line editor (e.g., Terminal), which will use the dependencies listed in the ```package.json``` to download all the necessary packages to each coders computer. That way, everyone has easy access to the required packages without storing huge folders on GitHub.
- ```npm uninstall package-name``` to uninstall.
- ```var lodash = require('lodash');```