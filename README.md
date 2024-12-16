requirement: We have a zip file which contains pdf files in it.pdf names contains customerno,year,month,cardtype.once the zip file uploaded to s3 source bucket s3 bucket will create event notification to sqs and sql will trigger lambda function and lambda fucntion will trigger the glue job with file name that was uploaded to s3 source bucket.
step1:-upload zip file to s3 bucket, once file uploaded it will trigger sqs.
step2:-sqs will trigger lambda function.
step3:-lambda will trigger the gluejob.
step4: glue job wil extract the zip file and uploads each pdf file to target s3 bucket wiht the folders /customerno/year/month/cardtype. these folder will be dynamically create in with gluejob
step5:once the gluejob is succes cloudeventbridge will trigger the success mail to respective team
