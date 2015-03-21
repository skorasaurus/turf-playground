# turf-playground

## What is this?

turf-playground is a project designed to let you play around and learn [turf](http://turfjs.org) in the browser without worrying about setting up the boilerplate code to get started. The playground is hosted at [turfjs.party](http://turfjs.party).

## Contributing

#### Technologies

turf-playground is built as a simple [AngularJS](http://angularjs.org) app. It uses [Browserify](http://browserify.org/) for building the compiled JS actually used by the site. Also:

- [Dox](https://github.com/tj/dox) for parsing comments in the turf code to generate the example code library
- [vm-browserify](https://github.com/tchannel/vm-browserify) for running editor code in an isolated context
- [ACE editor](http://ace.c9.io/) - the in-browser code editor

#### Running

Run the server using `npm start`

#### Building the project

turf-playground uses Browserify, so after changes are made to the `app/` code, you must run `npm run build`. This also reparses the JSDocs to build the turf examples library. The build script should always be run before the site is pushed.

#### Adding non-require-able js

If a library can't be used via `require` (due to the library's structure), the best option is to stick it in *public/vendor* and explicitly load the script in *index.html*
