# a-Bitcoin-blockchain-viewer-application
This project demonstrates basic interactions with a Bitcoin node using Python. It provides a simplified framework for connecting to Bitcoin nodes, sending and receiving messages, and parsing blockchain data.
## Overvie
The script connects to a Bitcoin node, sends a handshake, listens for messages, and interacts with blockchain data. It includes functionality to decode transaction and block information from the node's responses.
## Dependencies
   - Python 3.12+
   - `socket` for network connections
## Installation
To run this project, clone the repo and Run. No more dependency.
## Usage
Execute the main script to start interacting with a Bitcoin node:
`python main.py`
## Architecture Overview
The codebase is split into multiple modules:
   - `main.py`: Initializes the connection with Bitcoin node Domain.
   - `Connect2Net.py`: Handles network connections and message handling logic.
   - `Handshake.py`: Handshake with Bitcoin Node, Contains utility classes for encoding/decoding network messages.
   - `MessageHandler.py`: Encodes and decodes specific blockchain data structures.
## Test
Run the test function
`test_block_parse()`
```TestBlock
   Merkle Root: 01e5f8ef45651a8f28aac2691c0bf2159138400437274c02dd4b8b1ac2ef1564
   Timestamp: 1970-01-01 00:08:07
   Bits: 4294770688 (Difficulty: 0.0)
   Nonce: 2936209407
   Number of Transactions: 170
Transaction Information:
   Version: 7
   Locktime: 420741142
   Number of Inputs: 0
   Number of Outputs: 0
   Transaction Inputs:
   Transaction Outputs:
   Total Output Value: 0.54907064 BTC
Transaction Information:
   Version: 2839568471
   Locktime: 0
   Number of Inputs: 235
   Number of Outputs: 0
   Total Output Value: 0.54907064 BTC
   Transaction Inputs:
     Input 1:
      Previous Output Hash: 7601191df616bb9748bacd92b721a07b020000000000160014035a32e3e1d73f
      Output Index: 3973306363
      ScriptSig: c3a4a532a16fe4d70000000000fdffffff0200000000000000000a6a5d0714baa···
     Input 9:
      Previous Output Hash: 01f10b000000000000160014cdccb1311df1a421611dec5ac9ebc0a2ba219ac7
      Output Index: 0
============================== 1 passed in 0.10s ===============================
```
## Output Example
When running the script, you might see output similar to the following, indicating the interaction with the node:
```Main.py
Connected to Bitcoin node at 5.255.97.254:8333
Received version message: 80110100090400000000000000000000000000000···
Received verack message:
Connection established!
Received sendcmpct message: 000200000000000000
Received ping message: 91a6033e2dcc3a89
Sent Pong
Received feefilter message: e803000000000000
Received Inventory:  InvMessage(items=[(1, b'\xa7···f\x1cD\xf~')], command=b'inv')
Received tx message: [0100000001a7a81d4d8c0644ac1fb127a807d8ed97e35adb93f389dc377eb11d17f50ea5f3bf0000···]
Transaction Information:
  Version: 2
  Locktime: 0
  Number of Inputs: 1
  Number of Outputs: 2
  Total Output Value: 0.01094785 BTC
  Transaction Inputs:
    Input 1:
      Previous Output Hash: 6eb9c7438fe5cf86c6edf17005e2b7ea96cdb15adb9e4144411305fc5b6fc16c
      Output Index: 0
      ScriptSig: 
  Transaction Outputs:
    Output 1:
      Value: 49243 Satoshis (0.00049243 BTC)
      ScriptPubKey: 76a9149298be38e624dac4b0f159ae47f3eeedc04f381788ac
    Output 2:
      Value: 1045542 Satoshis (0.01045542 BTC)
      ScriptPubKey: 00147423a21054fcbb629602cfc94a1bd4c15e41fc57
 [Block ~~~ Showed in the Test  ~~~]
```
## Troubleshooting
 - Common issues include:
   - Connection issues: Need to connect more nodes, form peergroup, so as to be able to capture more Transaction and Block information faster, the network connection can also be more stable.
   - Added a test case: Utilizes a real block data example for parsing and validating the block information.
## Platform Compatibility
The code has been tested on the following platforms:
- macOS
- Linux
