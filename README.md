This is a small, quick 'n dirty example repository for building and uploading arbitrary helm charts to S3 buckets adhering to AWS' standard using `s3cmd`.

For documentation on configuration of `s3cmd`, please see:

- [Use s3cmd](https://github.com/marketplace/actions/use-s3cmd) (action documentation)
- [s3cmd's official documentation](https://s3tools.org/usage)

Basically, every configuration option/flag needed for `s3cmd` can just be provided as an Action Secret and added to the  action's definition in `.github/workflows/savehelmchart.yml`.

Secrets needed for the current version:

|Name|Usage|
|----|-----|
|AWS_REGION|Region of storage, if applicable|
|AWS_HOST|Host, in the format `http(s)://domain/ip`|
|AWS_ACCESS_KEY_ID|Access key|
|AWS_SECRET_ACCESS_KEY|Access secret|
|AWS_BUCKET|Bucket to use|