## Create a bucket

```sh
aws s3 mb s3://my-metadata-bucket-vs
```

## Create a text-file

```sh
echo "Hello World" > myfile.txt
```

## Put Object with metadata in the bucket

```sh
aws s3api put-object --bucket my-metadata-bucket-vs --key myfile.txt --body myfile.txt --metadata Planet=Mars
```

## Print out the head bucket to show metadata 

```sh
aws s3api head-object --bucket my-metadata-bucket-vs --key myfile.txt
```

## Delete object and bucket

```sh
aws s3 rm s3://my-metadata-bucket-vs/myfile.txt
aws s3 rb s3://my-metadata-bucket-vs
```