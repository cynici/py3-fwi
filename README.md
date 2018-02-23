# Canadian Forest Fire Weather Index calculator

Python3 implementation of the CAFWI calculator in Docker adapted from:
* https://github.com/buckinha/pyfwi
* https://code.google.com/archive/p/pyfwi/

The reference sample data may be found in `/tmp/pyfwi-master/testBatch.csv` 
Refer to https://github.com/Terranex/pyfwi/tree/master on how to create a CSV file containing a batch of test data.

## Background
- http://onlinelibrary.wiley.com/doi/10.1002/met.214/full 

## Usage

Sample `docker-compose.yml`

```
version: '2'
services:
  cafwi:
    image: cheewai/py3-fwi
    environment:
      - RUNUSER_UID=1000
    volumes:
      - ./:/home/runuser
    working_dir: /home/runuser
```
