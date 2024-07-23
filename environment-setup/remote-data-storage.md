# Remote Data Storage

### Remote Data Storage

Training workloads often rely on large data sets that can be cumbersome and expensive to move. Build AI offers a secure remote data storage solution to store all of your data and take advantage of our low cost training GPU cluster. Move your data once to Build AI’s secure storage for cheap and simplified access to your data during training.

On joining our private beta, your company was assigned a unique storage bucket and credentials. Our secure bucket storage uses the same API as Amazon S3. [Access the API docs here](https://docs.aws.amazon.com/pdfs/AmazonS3/latest/API/s3-api.pdf).

Once you have the [aws cli installed](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html), you can upload all files in a local directory to the bucket using the following command.

```bash
aws s3 sync /path/to/local/directory s3://your-bucket-name --endpoint-url <https://storage.trybuild.ai>
```

Note that our storage solution uses the AWS S3 API, but is not hosted or reliant on AWS in any way.
