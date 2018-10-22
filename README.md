# API backend
bitox.io site backend
API Documentation
API Endpoint
You can connect to Bitox.io's API through this endpoint:
https://backend.bitox.io/
Public API Methods
There is one public method, which take HTTP GET requests and return output in JSON format:
  
 <a href="https://backend.bitox.io/returnTicker">returnTicker</a>
    <p>This is standard returnTicker information including volume and price data. Returns the ticker for all markets. Sample output:</p>
    <p>{"ETH_0x8198e34": {"tokenAddr": "0x8198e349afd0a09efb06b460452ec1beab7a20aa", "quoteVolume": "500.0728741", "baseVolume": "0.2863036437", "last": "0.000050000000010000", "bid": "0.000050000", "ask": "0.0001", "updated": "2018-06-08T05:10:24.838277"}, [...]}</p>
  </ul>

##
# Web3
web3==3.16.4
eth_utils==0.7.4
# Require this until we upgrade above dependecies
eth-abi==0.5.0

##
# Sockets
# Lock yarl until aiohttp is fixed, cf. https://github.com/aio-libs/aiohttp/issues/2662
yarl==0.18.0
# Plain websockets for connections to the Ethereum node and orderbook observer
websockets~=4.0.1
# Socket.IO server to provide a WS API, backed by aiohttp for HTTP long-polling support
python-socketio~=1.8.4
aiohttp==2.3.7

##
# DB
# DB driver for application
asyncpg==0.14.0
# alembic for DB versioning
alembic==0.9.6
# For use with alembic
psycopg2~=2.7.3.2

##
# Queue
huey[backends]~=1.7.0
# For use with huey's redis backend
redis~=2.10.6
# Use greenlets for huey: our tasks are mostly I/O bound
gevent


##
# Data tools
# A data object validation tool:
cerberus==1.1

##
# Crypto tools
# ecrecover support:
coincurve>=7.0.0
rlp==0.4.7
