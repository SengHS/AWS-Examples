## Create a new s3 bucket

```md
aws s3 mb s3://checksums-examples-vs-1101
```

## create a file that will do a checksum on

```
echo "Hello Mars" > myfile.txt
```

## get a checksum of a file for md5

```
md5sum myfile.txt
```
#8ed2d86f12620cdba4c976ff6651637f  myfile.txt

## upload our s3 file to see

```
aws s3 cp myfile.txt s3://checksums-examples-vs-1101
aws s3api head-object --bucket checksums-examples-vs-1101 --key myfile.txt
```

## Lets upload a file with a different kind of checksum

```sh
sudo apt install rhash -y
rhash --crc32 --simple myfile.txt
echo "e7c80b87" | xxd -r -p | base64 #checksum value must be base64
```

```sh
aws s3api put-object \
--bucket checksums-examples-vs-1101 \
--key="myfilecrc32.txt" \
--body="myfile.txt" \
--checksum-algorithm="CRC32" \
--checksum-crc32="58gLhw=="  #copy the value from line32 output from bash
```
