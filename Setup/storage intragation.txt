
create  database health_db;
use database health_db;

create schema bronze;
use schema bronze;



CREATE OR REPLACE STORAGE INTEGRATION s3_int
TYPE = EXTERNAL_STAGE
STORAGE_PROVIDER = S3
ENABLED = TRUE
STORAGE_AWS_ROLE_ARN = 'arn:aws:iam::597601766568:role/healthcare'
STORAGE_ALLOWED_LOCATIONS = ('s3://healthcare-regex-2005/');



DESC INTEGRATION s3_int;


