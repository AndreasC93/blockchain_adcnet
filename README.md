# Proof of authourity blockchain_adcnet

## adcnet Configuration

Blocktime: 3 seconds
ChainID: 213
Node1 public key: 0xb30a7a853CADe248974429D7f1612e1F0c121f2E
Node1 password: admin
Node2 public key: 0xCD28B215A62A3F7CA4F4cB49aFd21D641d40A86A
Node2 password: admin
Port address: http://127.0.0.1.8545/

## Starting the Network

To start the adcnet POA blockchain network first open two separate terminal windows. In one window run the following command: "geth --datadir node1 --unlock "0xb30a7a853CADe248974429D7f1612e1F0c121f2E" --mine --rpc --allow-insecure-unlock". This will start up node 1 on adcnet. The --mine configures the node for mining while the --rpc allows the node to communicate with other nodes on the network. Note that --rpc is only needed for one node. 

To start node 2 run the command: "geth --datadir node2 --unlock "0xCD28B215A62A3F7CA4F4cB49aFd21D641d40A86A" --mine --port 30304 --bootnodes "enode://5638943adfba03764ff7f5401f191b72c220a7ffa10100185961b3fb400c5968fe7886fff64f2ec5ca9e7d77bfd7fcf3dcd072523aefb97290afdb739c03ec40@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock". Only --mine is needed to configure this node for mining. We have already configured rpc for node communication on node 1. Also note the enode from node 1 is included in node 2.

## Connecting MyCrypto

1 Open the MyCrypto at and navagate to "change network" under the MyCrypto logo in the bottom left menu of the app.
2 Select add custom node and use the adcnet configuration info above to activate. Make sure to change the "Network" dropdown to "custom" and type eth in the currency box.
3 Once all configuration information is entered click "save and use custom node".

## Sending Transactions

1 Open the MyCrypto app. Make sure you have started the network and are connected to the custom node as described above.
2 Navigate to "View and Send" on the left side of the screen and click on "Keystore File".
3 Select the keystore file for node1 or node2 depending on which account you want to send a transaction from and enter the password "admin". This will open the account in the MyCrypto app.
4 If you have opened node1 in my crypto you will paste the public key of node2 in the "To address" box. Enter the ammount of test tokens you would like to send, adjust the transaction fee as you see fit, and click "send transaction"
5 Click send in the popup window again and you should see a message that your transaction has been posted to the network.


