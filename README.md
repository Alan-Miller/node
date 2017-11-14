# Node
- Node is the JS engine outside the browser.
- npm is a Node package manager that lets us download and manage code packages other coders have written which we want to use in our project.

### Points to cover:
- Run JS in the command line editor (e.g., Terminal).
- Run a file using Node.
```js
    node index.js
```
- The ```package.json``` file holds metadata relevant to our project, including information about packages our project depends (i.e., our "dependencies").
- Use ```npm init``` to create package.json file. Hit ```Return``` several times afterward to skip ahead and say OK to the setup questions. Alternatively, instead of typing ```npm init```, type ```npm init -y``` to skip those questions.
```js 
    npm init -y 
```
- Use ```npm install package-name``` to install the package by name. This makes the package appear under the "dependencies" property in the ```package.json``` file.
```js
    npm install lodash
```
- At this point, make sure to have a file called ```.gitignore``` (no extension) in the project folder and to write ```node_modules``` on a new line inside that file. If the file is not there, create it and type ```node_modules``` inside. This will ensure Git ignores the node_modules folder and does not push it to GitHub. It is bad practice to put this folder (which can be very large) on GitHub. 
    Inside .gitignore file:
```js
    node_modules
```
- Use ```npm install``` to use the ```package.json``` file to determine what dependencies are required by the project and download them. Even though we use ```.gitignore``` to prevent ```node_modules``` from being pushed to GitHub, our ```package.json``` file is NOT ignored and IS pushed to GitHub, so when other coders clone our project, the ```package.json``` will be downloaded along with the project. They can then run ```npm install``` in their command line editor, which will use the dependencies listed in the ```package.json``` to download all the necessary packages to each coders computer. That way, everyone has easy access to the required packages without storing huge folders on GitHub.
```js
    npm install
```
- Use ```npm uninstall package-name``` to uninstall.
```js 
    npm uninstall lodash 
```
- Use ```var someVariable = require('some-node-modules-package');```
    - This syntax is how we reference a package we downloaded.
    - We require a node package by just using its name as it appears in the ```node_modules``` folder, surrounded by quotation marks. Notice there is no ```./```, which is what we would use to point to a file right in the same folder.
    Inside index.js file:
```js
    var lodash = require('lodash');
```