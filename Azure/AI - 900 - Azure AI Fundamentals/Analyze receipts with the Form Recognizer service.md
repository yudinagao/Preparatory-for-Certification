# Analyze receipts with the Form Recognizer service

## Azure Form recognizer

- Azure's Form Recognizer service can solve for this issue by digitizing fields from forms using optical character recognition (OCR)
- Azure's OCR technologies extract the contents and structure from forms, such as key, value pairs (eg. Quantity: 3)
    - name, address and telephone
    - date and time
    - quantity and price
    - subtotal, tax, total amount

Form recognizer
    - Matching fields names to values
    - Processing tables of data
    - Identifying specific types of field such as date, telephone, address, totals

Pre-built recepit model
- Time of transsaction
- data of transaction
- merchant information
- taxes paid
- receipt totals
- other information
- all text in receipt is recognized and returned too

- Images must be: JPEG, PNG, BMP, PDF , TIFF
- Size less than 50 MB
- 50x50 to 10000 x 10000 pixels
- pdf - 17 " x 17"

CUstom models
