# Open Hymn Format Binary Design

This document will outline the draft for the format binary design to allow reading and writing binary files using any programming language.

## Resource

* [Create Custom Binary Format](https://gamedevelopment.tutsplus.com/tutorials/create-custom-binary-file-formats-for-your-games-data--gamedev-206)

## Design Goals

* Attribution is the most important information to identify any hymn.  
  Key attribution info:
  * Hymn Title
  * Author Name
  * Composer Name
  * Release Year/Month
* Format should support versioning to allow format iterative improvements and backward compatibility.
* Support for RTL and non-Latin languages is a must.
* Optimize files for read and search even if it complicated file generation process.
* Allow collection of hymns in book-like structure.
* Indexing and searching is very important to searching between similar lyrics.

## Single Hymn Binary Format


### Header

```
HEADER
{
  signature  U24
  version    U8
}
```
`signature` will hold character codes for 3 ASCII characters that will represent the format "OHF".  
`version` will be 0 during format development, and start from 1 once this repo reaches first release.


### Attribution

```
ATTRIBUTION
{
  title         STRING
  author        STRING
  composer      STRING
  releaseDate   DATEYM
}
```
```
STRING
{
  dataLength  U16
  data        U8[dataLength]
}
```

```
DATEYM
{
  year  U16
  month U8
}
```
`realseDate` will have Year and Month instead of UNIX time-stamp because we expect some hymns dated before 1970. If the year or month  equals `00` then they are unknown.

Expected `author` and `composer` names:  

* heritage
* unknown


