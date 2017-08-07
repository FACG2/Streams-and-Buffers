## What are streams?
`const stream = require('stream')`

Streams are modules in `Node.js` that let you read data from a source or write data to a destination in a continuous fashion.


In `Node.js`, there are four types of streams:

  * Readable − Stream which is used for read operation.

  * Writable − Stream which is used for write operation.

  * Duplex − Stream which can be used for both read and write operation.

  * Transform − A type of duplex stream where the output is computed based on input.

Stream  read/write data chunk by chunk, without buffering the whole file at once.

In other words, if you read a textfile.txt where you have :
“Code Acdemy”. It is possible to consume the file at the pace of byte by byte (as 1 character is a byte) that allows you to grab, transform and display the contents of the file, byte by byte, progressively, like this:

* “character: C”
* “character: o”
* “character: d”
* “character: e”
* “character: “
* “character: A”
(…).

## Reading large files :

>  Streams are useful because they allow us to read bits of large files as soon as they're available.

### Efficient data flow :

  * stream.pipe(): limits the buffering of data to acceptable levels
  * highWaterMark: sets a threshold to stop reading data until it is consumed

## What are buffers?

Transferring a big amount of data after converting it into small chunks of data. These small chunks can be used simultaneously, without waiting for the whole amount of the data to download.

> For example - Watching a youtube video,without downloading the whole file.

Streams also use buffers (typically), to store content streamed so far, and when the stream is done, that buffer gets freed somewhere (examples: in case of reading, freed up in the output device, case of writing; writing to the disk).
_
