# karma-global-preprocessor

> Preprocessor which makes variables globally available in your tests

## Installation

    npm install karma-global-preprocessor --save-dev

## Configuration

    module.exports = function (config) {
        config.set({
            ... 
            
            // Set globally available variables
            globals: {
                'MY_VAR': 123
            },
            
            // Add plugin to karma
            plugins: [
                ...
                'karma-global-preprocessor',
                ...
            ],
            
            // Select the file where we will insert the definition of global variables
            preprocessors: {
                'index.js': ['global']
            }
            
            ...
        });
    };

## Using

Now, you will be able to use the variable via `window.globals.MY_VAR` and it will be `123`!
