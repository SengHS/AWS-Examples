## Create a s3 bucket

```sh
aws s3 mb s3://storage-class-vs-1101
```

## Create a file and put it into a STANDARD_IA storage class

```sh
echo "Hello World!" > mytext.txt
aws s3api put-object --bucket storage-class-vs-1101 --key hello.txt --body mytext.txt --storage-class STANDARD_IA
```

## Clean Up

```sh
aws s3 rm s3://storage-class-vs-1101/hello.txt
aws s3 rb s3://storage-class-vs-1101
```