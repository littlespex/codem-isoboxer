# codem-isoboxer

* http://github.com/madebyhiro/codem-isoboxer

## Description

Codem-isoboxer is a small browser-based MPEG-4 (ISOBMFF) parser. Currently a limited set of ISOBMFF boxes is supported:

* free/skip
* ftyp
* moov
* mvhd
* tkhd
* trak

Support for more boxes can easily be added by adding additional box parsers in `src/iso_box.js`.

## Requirements

Modern web browser with support for:

* ArrayBuffer
* DataView

## Usage

Include one of the files in the `dist` folder (regular or uglified) in your web page/application:

    <script type="text/javascript" src="iso_boxer.min.js"></script>

Then, you can parse a file by calling the `create` function:

    var parsedFile = ISOBoxer.create(arrayBuffer);

The `arrayBuffer` can for example be obtained by issuing an XHR request, or by using the `FileReader` API to read a local file.

## Development

Check out the source from Github. Make changes to the files in `/src`. We use `grunt` to build the distribution files.

### Building

    grunt

### Using grunt watcher

You can use `grunt-contrib-watch` to watch for changes to the source and automatically build it:

    grunt watch

## Demo

Open `test/index.html` in your browser. Use the file picker to select a local MPEG-4 file and parse it. Results will be in the `window.parsedFile` variable. Inspect it from your browser's console.

## License

Codem-isoboxer is released under the MIT license, see `LICENSE.txt`.
