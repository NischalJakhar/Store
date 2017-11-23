# Store

*master.dust* is main layout file that will include things like nav bar etc.
*index.dust* is a 4 column layout where books are placed.
*style.css* is our css file which we wrote for master.dust and index.dust.




``Options``  https://github.com/krakenjs/kraken-js

Pass the following options to kraken via a config object such as this:

var options = {
    onconfig: function (config, callback) {
        // do stuff
        callback(null, config);
    }
};

// ...

app.use(kraken(options));

Note: All kraken-js configuration settings are optional.
================================================================================================================
onconfig (Function, optional)

Provides an asynchronous hook for loading additional configuration. When invoked, a confit configuration object containing all loaded configuration value passed as the first argument, and a callback as the second. The signature of this handler is function (config, callback) and the callback is a standard error-back which accepts an error as the first argument and the config object as the second, e.g. callback(null, config).
============================================


*lib/db.js* has our db connections inside a db function with config and shit cuz of the krakenjs.This file is required in index.js and inside options var we do the shit as written above.
