# ruby-aws
A quick repo to play with AWS in Ruby
It supports creating buckets, uploading files to a bucket, listing files in a bucket, 


##Usage
ruby ./ruby-aws bucket_name [operation] [options]

```
Where:
  bucket_name (required) is the name of the bucket

  operation   is the operation to perform on the bucket:
              create   - creates a new bucket
              upload   - uploads a file to the bucket
              list     - (default) lists up to 50 bucket items
              get      - Retrieves a file from the bucket, and prints it.
              download - Retrieves a file from the bucket, and downloads it.

  file_name   is the name of the file to upload,
              required when operation is 'upload'

Operations with specific arguments:
  get         - requires a following argument: filename.
                Ex: ./ruby-aws bucket-name get #{filename}

  download    - requires two arguments: filename, localPath
                Ex: ./ruby-aws bucket-name download #{filename} #{localPath}
                    ./ruby-aws test-bucket download helloworld.txt "./helloworld.txt"
```

Followed tutorials:
https://aws.amazon.com/blogs/developer/downloading-objects-from-amazon-s3-using-the-aws-sdk-for-ruby/

https://docs.aws.amazon.com/sdk-for-ruby/v3/developer-guide/hello.html
