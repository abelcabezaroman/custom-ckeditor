clone the ckeditor5-build-classic

git clone -b stable https://github.com/ckeditor/ckeditor5-build-classic.git
cd ckeditor5-build-classic
install dependencies and any other plugins you may want to add (alignment for instance)

npm i
 npm install --save-dev @ckeditor/ckeditor5-alignment

update src/ckeditor.js with added plugin(s)

import Alignment from '@ckeditor/ckeditor5-alignment/src/alignment';

// Plugins to include in the build.
ClassicEditor.builtinPlugins = [
    ...
    Alignment                                                            
];
run npm run buildto package the new build

copy the file build/ckeditor.js to the asset folder in you angular application

This is how you import the file (path may vary depending on your setup) :

import * as CustomEditor from '@app/../assets/ckeditor.js';

Finally in your component just declare the editor like this :

public Editor = CustomEditor;
#   c u s t o m - c k e d i t o r  
 #   c u s t o m - c k e d i t o r  
 