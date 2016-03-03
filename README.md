# emaf

## What
Parser against Vantiv's 8583 specification. File is the response for the daily capture/settlement requests. 

File has transaction-level interchange details in it, allowing for transaction-level costs. 

Import parsed data and ETL production data and join for reports that have Volume, Revenue, and Costs grouped by sub merchant. Incredible business intelligence. 

## Instructions
````
$ postgres -D /usr/local/var/postgres9.5/ &

$ npm install

$ cd automation ; ./parse.sh

````

## To do
- [X] Parse file
- [X] ETL production data into datamart
- [X] create join of production data to parsed EMAF data
- [ ] turn fixed-length of TransferLog Id (string) into an integer without data loss, and concationate again to TransferLog ClassId for string
-	[ ] interchange qualification code
- [ ] model assessments
- [ ] model cross border surcharges
- [X] schedule nightly ETL
