# S3 Python Examples
Example functions for reading and writing from an S3 bucket

## Prerequisites
Install and configure the AWS CLI: https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

## Functions
### read_file_from_s3
This Python script includes a function called read_file_from_s3 that reads a file from an Amazon S3 bucket and saves it to a local directory. Here are the main steps of the function:

1. The read_file_from_s3 function takes three parameters: s3_bucket_name, s3_object_key, and local_directory.
2. The function creates an S3 client using boto3.
3. It uses the get_object method of the S3 client to retrieve the file from the specified S3 bucket with the specified object key.
4. It constructs the local file path by joining the local_directory and s3_object_key parameters using the os.path.join method.
5. It writes the contents of the file to the local directory using the write method of a file object.
6. If successful, it prints a success message with the local file path where the file was saved.
7. If unsuccessful, it prints an error message.
8. The script also includes an example usage of the read_file_from_s3 function, where the function is called with appropriate parameters to read a file from an S3 bucket and save it to a local directory.

### write_file_to_s3
This Python script includes a function called write_file_to_s3 that uploads a local file to an Amazon S3 bucket. Here are the main steps of the function:

1. The write_file_to_s3 function takes two parameters: local_file_path and s3_bucket_name.
2. The function creates an S3 client using boto3.
3. It uses the os.path.basename method to get the file name from the local_file_path parameter.
4. It uses the upload_file method of the S3 client to upload the file to the specified S3 bucket with the same object key as the local file name.
5. If successful, it prints a success message.
6. If unsuccessful, it prints an error message.
7. The script also includes an example usage of the write_file_to_s3 function, where the function is called with appropriate parameters to write a local file to an S3 bucket.