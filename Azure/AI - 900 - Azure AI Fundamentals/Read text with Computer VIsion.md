# Read text with Computer VIsion

## Read API on Azure

- Uses the lastest recognition models and optimized for images with significant amount of the or considerable visual noise
- can handle scanned documents with have a lot of text
    - automatically determine proper recognition
        - printed tet or handwriting
- large documents
- works asynchronous
    - submit an image to api and retrieve operation id in response
    - use id to check the status of the imagen until its completed
    - retrieve the results - hierarchy
        - Pages
            - one for each page of text, including orientation and page size
        - lines
            - lines of text on a page
        - words
            - the words in a line of text, including bounding box coordinates and the text itself