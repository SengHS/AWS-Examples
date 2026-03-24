# Create a bucket
```sh
aws s3 mb s3://my-example-prefixes-bucket-vs
```


# Create a "Folder"
```sh
aws s3api put-object --bucket my-example-prefixes-bucket-vs --key hello/
```


# Create many "Folder" with the limit of 1024 byte
```sh
aws s3api put-object --bucket my-example-prefixes-bucket-vs --key Lorem/ipsum/dolor/sit/amet/consectetur/adipiscing/elit/In/at/orci/maximus/mi/rhoncus/venenatis/eget/ut/quam/Aliquam/erat/volutpat/Morbi/laoreet/ut/mi/sed/molestie/Ut/viverra/semper/dolor/eget/ornare/neque/volutpat/convallis/Mauris/porta/magna/et/felis/venenatis/nec/porta/lacus/rhoncus/Duis/interdum/aliquam/mattis/Pellentesque/et/massa/dictum/finibus/massa/quis/tincidunt/enim/In/hac/habitasse/platea/dictumst/Donec/faucibus/nisi/vel/nisi/tincidunt/eget/vehicula/neque/tincidunt/Pellentesque/tincidunt/massa/sed/euismod/varius/elit/velit/tempus/turpis/quis/ullamcorper/arcu/risus/vel/massa/Curabitur/convallis/ipsum/eget/erat/consectetur/tempus/Mauris/nec/aliquet/risus/In/hac/habitasse/platea/dictumst/Maecenas/ullamcorper/elementum/euismod/Nullam/vel/magna/fringilla/malesuada/orci/eu/tempor/mauris/Cras/sed/blandit/turpis/a/hendrerit/nulla/Sed/id/facilisis/erat/Phasellus/imperdiet/felis/maximus/vehicula/consequat/purus/turpis/rhoncus/enim/ut/commodo/erat/erat/id/purus/Orci/varius/biam/what/are/you/thinking/hell/this/
```

# Breaking the 1024 limit in S3 Folder name (added more folder to ensure the limit hitted)
```sh
aws s3api put-object --bucket my-example-prefixes-bucket-vs --key Lorem/ipsum/dolor/sit/amet/consectetur/adipiscing/elit/In/at/orci/maximus/mi/rhoncus/venenatis/eget/ut/quam/Aliquam/erat/volutpat/Morbi/laoreet/ut/mi/sed/molestie/Ut/viverra/semper/dolor/eget/ornare/neque/volutpat/convallis/Mauris/porta/magna/et/felis/venenatis/nec/porta/lacus/rhoncus/Duis/interdum/aliquam/mattis/Pellentesque/et/massa/dictum/finibus/massa/quis/tincidunt/enim/In/hac/habitasse/platea/dictumst/Donec/faucibus/nisi/vel/nisi/tincidunt/eget/vehicula/neque/tincidunt/Pellentesque/tincidunt/massa/sed/euismod/varius/elit/velit/tempus/turpis/quis/ullamcorper/arcu/risus/vel/massa/Curabitur/convallis/ipsum/eget/erat/consectetur/tempus/Mauris/nec/aliquet/risus/In/hac/habitasse/platea/dictumst/Maecenas/ullamcorper/elementum/euismod/Nullam/vel/magna/fringilla/malesuada/orci/eu/tempor/mauris/Cras/sed/blandit/turpis/a/hendrerit/nulla/Sed/id/facilisis/erat/Phasellus/imperdiet/felis/maximus/vehicula/consequat/purus/turpis/rhoncus/enim/ut/commodo/erat/erat/id/purus/Orci/varius/biam/what/are/you/thinking/hell/this/are/you/exceeding/the/limit --body myfile.txt 
```




