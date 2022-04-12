# Private Blockchain Project 
Udacity Blockchain Project 1 v2
Private Blockchain Application  v1.1
v
-----------Resubmitt, all Change Requests completed, summary below: (4/12/2022)
 
CR PBC001 (BlockchainController) added missing endpoint, see outputs below and screenshots file for trigger from ThunderClient
CR PBC002 (Blockchain) replaced Filter with Find
CR PBC003 (Block) replace long hand variable assignments with rest spread operator

(app.js)  added debug npm and will leave console.log in place for now to avoid others environment config

complete regression test of all requirements below:

get block zero:

{
  "hash": "fd9a719eeb7288feff9a620ec6904f709859215731ceec638037b3fdf68d0532",
  "height": 0,
  "body": "7b2264617461223a2247656e6573697320426c6f636b227d",
  "time": "1649774782",
  "previousBlockHash": null
}


RequestValidation:

"mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz:1649774898:starRegistry"

submitt 2 stars:
{
  "hash": "fb19a391ae6c8fe69f2a471f3586d5fc39b645df4f592f5f01d36cdd1c189ace",
  "height": 2,
  "body": "7b226f776e6572223a226d7271444a4e6667387054477554385a78484a58424a43536d74777352364376477a222c2273746172223a7b22646563223a223638c2b0203532272035362e39222c227261223a223136682032396d20322e3173222c2273746f7279223a225465737420537461722032227d7d",
  "time": "1649774963",
  "previousBlockHash": "c3d43755fe495d4668e8f287d0ba1ded4aa371a0cd6b4d9a73d8b46058da9b70"
}


retrieve stars:
[
  {
    "owner": "mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz",
    "star": {
      "dec": "68Â° 52' 56.9",
      "ra": "16h 29m 1.1s",
      "story": "Test Star 1"
    }
  },
  {
    "owner": "mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz",
    "star": {
      "dec": "68Â° 52' 56.9",
      "ra": "16h 29m 2.1s",
      "story": "Test Star 2"
    }
  }
]

validate chain:

Valid Chain Found

Additional Configuration Information :

Thunder Client (postman alternative) JSON for get/post:

{"client":"Thunder Client","collectionName":"udacity blockchain","dateExported":"2022-04-12T14:55:57.000Z","version":"1.1","folders":[],"requests":[{"_id":"f1c1516e-82fe-4857-a26d-e594c89d88d9","colId":"1475062e-9293-435c-8a52-0fd79eac31c6","containerId":"","name":"http://localhost:8000/block/height/0","url":"http://localhost:8000/block/height/0","method":"GET","sortNum":10000,"created":"2022-04-10T18:09:14.463Z","modified":"2022-04-12T00:16:25.065Z","headers":[],"params":[],"body":{"type":"json","raw":"{\n\"address\":\"bc1qvmzkj4k6u8nqk9jt8zk5tf7src0qh2wxxvcs89\"\n}","form":[]},"tests":[]},{"_id":"7c8d7c2d-e4ae-49b7-bfa6-44057f171224","colId":"1475062e-9293-435c-8a52-0fd79eac31c6","containerId":"","name":"http://localhost:8000/requestValidation","url":"http://localhost:8000/requestValidation","method":"POST","sortNum":20000,"created":"2022-04-10T23:35:05.056Z","modified":"2022-04-11T01:06:05.231Z","headers":[],"params":[],"body":{"type":"json","raw":"{\n    \"address\":\"mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz\"\n}","form":[]},"tests":[]},{"_id":"8682e360-8dbd-408b-b7d0-703a7e9e10b7","colId":"1475062e-9293-435c-8a52-0fd79eac31c6","containerId":"","name":"http://localhost:8000/submitstar","url":"http://localhost:8000/submitstar","method":"POST","sortNum":30000,"created":"2022-04-11T00:05:50.690Z","modified":"2022-04-12T14:49:23.768Z","headers":[],"params":[],"body":{"type":"json","raw":"{\n    \"address\":\"mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz\",\n    \"message\":\"mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz:1649774898:starRegistry\",\n    \"signature\":\"H8SiC08C48w46VBnD/fcbiLnuIVpe70dimVfiQtybi7DA3cPxvYf0MpsNyCcNeuCeBoazTVucSLeEWTHO/0Dhxs=\",\n    \"star\": {\n            \"dec\": \"68° 52' 56.9\",\n            \"ra\": \"16h 29m 2.1s\",\n            \"story\": \"Test Star 2\"\n\t\t}\n}","form":[]},"tests":[]},{"_id":"5e241e99-f551-41df-87cb-70f435360709","colId":"1475062e-9293-435c-8a52-0fd79eac31c6","containerId":"","name":"http://localhost:8000/GetStarByAddress","url":"http://localhost:8000/blocks/mrqDJNfg8pTGuT8ZxHJXBJCSmtwsR6CvGz","method":"GET","sortNum":40000,"created":"2022-04-11T01:41:15.771Z","modified":"2022-04-11T03:42:11.442Z","headers":[],"params":[],"tests":[]},{"_id":"dcb8bf65-7c0d-41bf-9d4b-48a5d1ef0d92","colId":"1475062e-9293-435c-8a52-0fd79eac31c6","containerId":"","name":"http://localhost:8000/ValidateChain","url":"http://localhost:8000/validateChain","method":"GET","sortNum":50000,"created":"2022-04-11T23:35:14.757Z","modified":"2022-04-11T23:36:49.595Z","headers":[],"params":[],"tests":[]}]}

 


----------------------------------------
Original Submission 4/11/2022

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




