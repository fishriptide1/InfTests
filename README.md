# Private Blockchain Project 
Udacity Blockchain Project 1 v2
Private Blockchain Application

Development environment used VS Code + Thunder Client.  Screen shots and copy/paste of each get/post operation included in .pdf README in order provided by course documentation.  

Get Height
{
  "hash": "69660ab8739427caa987c4291282d71fc350dffb7a33a45f99d322fe375c3f8f",
  "height": 0,
  "body": "7b2264617461223a2247656e6573697320426c6f636b227d",
  "time": "1649695555",
  "previousBlockHash": null
}

 

Request Validation
"mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz:1649695665:starRegistry"
 

Submit 4 stars:
{
  "hash": "43a167bf519ed3e309256dd05efac608e1c9f9735da7ed6f4298b209e3dcd372",
  "height": 4,
  "body": "7b226f776e6572223a226d7271444a4e6667387054477554385a78484a58424a43536d74777352364376477a222c2273746172223a7b22646563223a223638c2b0203532272035362e39222c227261223a223136682032396d20342e3473222c2273746f7279223a225465737420537461722034227d7d",
  "time": "1649695813",
  "previousBlockHash": "945fe825a34177c8731c31d916fc94523ec0ab78d72854c34365254b57a497da"
}

 
 

Get Star by Address
[
  {
    "owner": "mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz",
    "star": {
      "dec": "68Â° 52' 56.9",
      "ra": "16h 29m 1.0s",
      "story": "Test Star 1"
    }
  },
  {
    "owner": "mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz",
    "star": {
      "dec": "68Â° 52' 56.9",
      "ra": "16h 29m 2.2s",
      "story": "Test Star 2"
    }
  },
  {
    "owner": "mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz",
    "star": {
      "dec": "68Â° 52' 56.9",
      "ra": "16h 29m 3.3s",
      "story": "Test Star 3"
    }
  },
  {
    "owner": "mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz",
    "star": {
      "dec": "68Â° 52' 56.9",
      "ra": "16h 29m 4.4s",
      "story": "Test Star 4"
    }
  }
]

 


Thunder Client config (instead of Postman)
 


Feedback:

The overall layout, source code files, readme and instructions are all excellent, only the address signing activities needs to be updated due to deficiencies in the Electrum wallet.  From my limited research it appears difficult to obtain legacy addresses from Electrum and other wallets making the address invalid when trying to sign the message for the final steps of the project post operations.  There are many simplified options available, one of which is to use Bitcoin core itself.  I recommend updating the content with a different mechanism as to keep the focus on the code and not on operational issues that are not as valuable.

Must use command line with legacy to get valid address for use with Bitcoin Core
bitcoin-cli -testnet getnewaddress "" legacy
 
 
 Udacity Blockchain Project 1 v2
Private Blockchain Application

Development environment used VS Code + Thunder Client.  Screen shots and copy/paste of each get/post operation included below in order provided by course documentation.  

Get Height
{
  "hash": "69660ab8739427caa987c4291282d71fc350dffb7a33a45f99d322fe375c3f8f",
  "height": 0,
  "body": "7b2264617461223a2247656e6573697320426c6f636b227d",
  "time": "1649695555",
  "previousBlockHash": null
}

 

Request Validation
"mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz:1649695665:starRegistry"
 

Submit 4 stars:
{
  "hash": "43a167bf519ed3e309256dd05efac608e1c9f9735da7ed6f4298b209e3dcd372",
  "height": 4,
  "body": "7b226f776e6572223a226d7271444a4e6667387054477554385a78484a58424a43536d74777352364376477a222c2273746172223a7b22646563223a223638c2b0203532272035362e39222c227261223a223136682032396d20342e3473222c2273746f7279223a225465737420537461722034227d7d",
  "time": "1649695813",
  "previousBlockHash": "945fe825a34177c8731c31d916fc94523ec0ab78d72854c34365254b57a497da"
}

 
 

Get Star by Address
[
  {
    "owner": "mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz",
    "star": {
      "dec": "68Â° 52' 56.9",
      "ra": "16h 29m 1.0s",
      "story": "Test Star 1"
    }
  },
  {
    "owner": "mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz",
    "star": {
      "dec": "68Â° 52' 56.9",
      "ra": "16h 29m 2.2s",
      "story": "Test Star 2"
    }
  },
  {
    "owner": "mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz",
    "star": {
      "dec": "68Â° 52' 56.9",
      "ra": "16h 29m 3.3s",
      "story": "Test Star 3"
    }
  },
  {
    "owner": "mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz",
    "star": {
      "dec": "68Â° 52' 56.9",
      "ra": "16h 29m 4.4s",
      "story": "Test Star 4"
    }
  }
]

 


Thunder Client config (instead of Postman)
 


Feedback:

The overall layout, source code files, readme and instructions are all excellent, only the address signing activities needs to be updated due to deficiencies in the Electrum wallet.  From my limited research it appears difficult to obtain legacy addresses from Electrum and other wallets making the address invalid when trying to sign the message for the final steps of the project post operations.  There are many simplified options available, one of which is to use Bitcoin core itself.  I recommend updating the content with a different mechanism as to keep the focus on the code and not on operational issues that are not as valuable.

Must use command line with legacy to get valid address for use with Bitcoin Core
bitcoin-cli -testnet getnewaddress "" legacy
 

[README.pdf](https://github.com/fishriptide1/project_1_v2_boilerplate/files/8467614/README.pdf)




