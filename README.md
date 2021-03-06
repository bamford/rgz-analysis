rgz-analysis
============

Analysis pipeline for Radio Galaxy Zoo.

Requires:

- mongodb
- Python with numpy, astropy, matplotlib, pandas, pymongo, scipy packages

To set up the pipeline, you will need a download of the database from the Amazon S3 servers. This is obtained via email link; contact the Zooniverse team at Adler for this. As of mid-Jan 2014, the raw database (which is a set of BSON and JSON files generated by mongoexport) is several hundred MB. 

Once the database is downloaded, the pipeline can be run by:

- run a ```mongod``` session on your local machine
- run ```mongorestore``` on all three BSON collection files (radio_classifications, radio_subjects, radio_users). Example:
    ```mongorestore --db ouroboros --drop --collection radio_users radio_2014-01-05/radio_users.bson```
- run ```python rgz.py```
