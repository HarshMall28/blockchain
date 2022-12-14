## Install python on your system via packager or from the web ##

## Install pip3 ##
``` sudo apt install python3-pip```

## Install Web3 ##
``` pip3 install web3 ```

For mac users

``` python3 -m pip install web3 ```


## Install decouple ##
``` pip3 install python-decouple ```

## Create an .env file and import items to it  ##

<img width="611" alt="Screenshot 2022-12-14 at 16 09 46" src="https://user-images.githubusercontent.com/118826262/207647890-2c7d078e-2a42-4de5-9668-71f278e6b517.png">

INFURA_URL is the URL we will use to gain access to Infura’s ethereum nodesCONTRACT_ADDRESS is the address of your deployed token smart contractOWNER_ADDRESS is the address you used to deploy the contractSUPER_SECRET_PRIVATE_KEY is your OWNER_ADDRESS private key (from metamask)


## Imports ##
<img width="459" alt="Screenshot 2022-12-14 at 16 12 01" src="https://user-images.githubusercontent.com/118826262/207648756-e0b60a19-50ec-4d35-aeab-9fc6e34b0406.png">

Import web3 and config from decouple and config gives us he .env functionality.

## Set up envronment variables ##

<img width="611" alt="Screenshot 2022-12-14 at 16 09 46" src="https://user-images.githubusercontent.com/118826262/207647890-2c7d078e-2a42-4de5-9668-71f278e6b517.png">

Setup the following variables as shown in the figure. abi can be found on the etherscan website. refer the following diagram.

<img width="1101" alt="Screenshot 2022-12-14 at 16 18 21" src="https://user-images.githubusercontent.com/118826262/207650240-9b8083c9-1c9c-4642-b2f9-499900bb2387.png">

## Run the eth_transfer.py file ##

``` python3 eth_transfer.py ```

## Build an Image ##

```docker build --tag [repositoryName]/[imageName]:tagName .```


## Run an image ##

```docker run --name [repositoryName] -p 8090:8080 [imageName]```

## Run the curl command ##

This transfers ETH:

```curl --header "Content-Type: application/json" --request POST --data '{"address":"0xac4FafdA6A3A6B48b4cDC2a896acf8D104C81d6C", "amount":"0.05"}' http://localhost:8090/eth```

This transfers token:

```curl --header "Content-Type: application/json" --request POST --data '{"address":"0xac4FafdA6A3A6B48b4cDC2a896acf8D104C81d6C"}' http://localhost:8090/token```

