# Detego Stocktake Read Events Dataset

**Note: As this paper is currently under review, this repository does only contain a sample of the dataset.**

This dataset was introduced in the paper "RFID in the Wild - Analyzing Stocktake Data to Determine Detection Probabilities of Products", and consists of two parts:

1. Information about the individual stocktakes
2. The read events of individual stocktakes 

Specifically, the dataset contains the following information about individual stocktakes in the `sample_stocktakes.csv` file:

* InventoryId: the unique identifier of a stocktake
* Store: the unique identifier of the store in which the stocktake was performed
* Region: the region in which the store is located in (i.e., US, Europe, or Asia)
* Expected: the number of items which were expected by the stock management system for the stocktake
* Unexpected: the number of items which were not expected by the stock management system for the stocktake
* Missing: the number of items which were expected by the stock management system but not found for the stocktake
* Actual: the number of items which were actually read during the stocktake
* TimeStampStart and TimeStampEnd: the timestamps in UTC time when the stocktake started/was finished
* Accuracy: the achieved accuracy of the stocktake (determined by the item quantities)

Furthermore, for each stocktake all recorded items are available as well in the `sample_read_events.csv` file. It contains:

* InventoryId: the unique identifier of a stocktake
* EpcSerial: the unique identifier of an item (EPC without company prefix)
* Product: the identifier of the product the item is associated with

