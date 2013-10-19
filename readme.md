dropzone
==============

Nette tool for uploading files using dropzone.js


Dependencies
-----

- http://www.dropzonejs.com
- http://www.aviary.com/


Instalation
-----

composer.json

    "ondrs/dropzone": "dev-master"

Usage
-----

Register service in your config.neon.
Set www dir and Aviary key.

    dropzoneFactory: ondrs\dropzone\Factory(%wwwDir%, %aviaryKey%)


Create dropzone component in presenter

    $this['dropzone'] = $this->dropzoneFactory->create('/path/to/dir');


Set form text input

    $this['dropzone']->setInput( $this['form']['image'] );