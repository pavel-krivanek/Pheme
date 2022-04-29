# Pheme
A simple implementation of a mini Scheme described in [this book](https://books.pharo.org/booklet-AMiniSchemeInPharo/).

OSX builds
Master: [![Build Status](https://travis-ci.org/Ducasse/Pheme.svg?branch=master)](https://travis-ci.org/Ducasse/Pheme)

Coverage:
[![Coverage Status](https://coveralls.io/repos/github/Ducasse/Pheme/badge.svg)](https://coveralls.io/github/Ducasse/Pheme)

## How to load 
Pharo 6.1:
```smalltalk
Metacello new
   baseline: 'Pheme';
   repository: 'github://Ducasse/Pheme/src';
   load.
```
Newer Pharo releases:
```smalltalk
Metacello new
   baseline: 'OldCompiler';
   repository: 'github://pharo-project/OldCompiler/src';
   load.

Metacello new
   baseline: 'Pheme';
   repository: 'github://Ducasse/Pheme/src';
   load.
```

## Example

```smalltalk
Phsyche new parseAndEval: '
(begin 
	(define squared (lambda (x) (* x x))) 
	(squared 2))'.
```


