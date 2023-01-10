# Azure Storage REST API Reference

## Blobs
Using the REST API
- Devs can create a hierarchical namespace similar to a file system
- block blobs can be created in two ways
    - upload using a single Put Blob operation
    - upload a blob as a set of block with a put block and commit the blocks to a blob with put block list
- page blobs are created and initialized 
    - with maximum size with a call to put blob
    - to wirte, use the put page operation
- append blobs
    - created using put blob
    - append blob does not include content using put blob
    - to write content use append block
    - delete of update not available
blobs can be read using get blob

## Queues

## Table Service

## File Service
