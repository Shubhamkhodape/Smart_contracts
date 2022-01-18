# Flutter application with smart contract
 

## Objective
   To understand steps for initializing this project.

## Some Important points
Ethereum Blockchain - Ethereum is a decentralized blockchain platform that establishes a peer-to-peer network that securely executes and verifies application code, called smart contracts. Smart contracts allow participants to transact with each other without a trusted central authority. 

Smart contracts - Smart contracts are the fundamental building blocks of Ethereum applications. They are computer programs stored on the blockchain that allows us to convert traditional contracts into digital parallels. Smart contracts are very logical - following an if this then that structure. This means they behave exactly as programmed and cannot be changed.

Web3Dart - It is a dart library that connects to interact with the Ethereum blockchain. It connects to an Ethereum node to send transactions, interact with smart contracts, and much more!      

Truffle Suite-  A world-class development environment, testing framework, and asset pipeline for blockchains using the Ethereum Virtual Machine (EVM). 

Ganache - A personal blockchain for Ethereum development you can use to deploy contracts, develop your applications, and run tests. It is available as both a desktop application as well as a command-line tool (formerly known as the TestRPC).



## Instructions
Step 1  -  Initialize the flutter project on Visual studio Code by cloning the project.

![2](https://user-images.githubusercontent.com/86108765/149812214-56171f39-54d0-4de5-bb31-1f199afe06f8.png)

Step 2 - Install Truffle.
-run this command at the terminal.
```bash
 npm install truffle -g
```
Next, go inside the migrations folder and create a new file, named 2_deploy_contracts.js


Step 3 - Install Ganache and deploy smart contract.
![Ganache](https://user-images.githubusercontent.com/86108765/149814230-38e2f18d-b5c9-47c7-a193-3ff8e4a75db2.png)

Create a new workspace.

Add workspace name.

Click on the add Project.


![ganache1](https://user-images.githubusercontent.com/86108765/149814360-4516bc25-98ae-4549-adce-fc7a5e87a43a.png)

Go to the Project folder and select the truffle-config.js file.

And click on the save workspace



![ganache2](https://user-images.githubusercontent.com/86108765/149814374-0b75a9ae-35a3-4531-a556-a6fa57e651fd.png)

In truffle-config.js, we need to do some configurations.

![config](https://user-images.githubusercontent.com/86108765/149815181-dc0b5678-f187-4f88-a598-fa222f681a40.png)

we have to provide the host, port number, and Network id which we will be getting from the ganache.

Ganache-> server.

we need to provide the directory where our Contract Application Binary Interface (ABI) will be stored. It is the standard way to interact with contracts in the Ethereum ecosystem.

![ganche3](https://user-images.githubusercontent.com/86108765/149815540-c66379f2-64dd-4658-9e96-fe3907dee6e3.png)

Lastly, deploy the contract.
```bash
truffle migrate
```

deployment output-

![deployment ss](https://user-images.githubusercontent.com/86108765/149816006-d0188444-3108-431e-828b-afec5c9c8eee.png)

Step 4 -Setting up Flutter to interact with Smart Contract.
Firstly we will need to have main packages Web3dart and http.

Initialize the Client.

we need to provide an RPC URL in main.dart file.

![main1](https://user-images.githubusercontent.com/86108765/149816431-70720d9e-6a62-41a2-b3d9-be010d92c5cf.png)

This will start a client that connects to a JSON RPC API, available at the RPC URL. The HTTP client will be used to send requests to the RPC server.0

We will get the above RPC URL from Ganache:

![ganache4](https://user-images.githubusercontent.com/86108765/149816990-143eb69f-acfd-48d9-9362-50f82f5a7bd7.png)

Then, we can distribute the initialization process and in main.dart file provide a private key of the user.

![main3](https://user-images.githubusercontent.com/86108765/149817124-b3fd81a7-1f1a-4356-98dd-dd2ca3e369e6.png)

We will get this private Key from Ganache:

![privatekey](https://user-images.githubusercontent.com/86108765/149817347-b90fc499-10f2-413e-8107-caa3ab1d3277.png)

Also, to allow Flutter to read the ABI, in pubspec.yaml, add this to assets:

![src](https://user-images.githubusercontent.com/86108765/149818930-dcdb03be-c577-4190-9927-f2612ff2be51.png)


Lastly, to start the application.

```bash
flutter run
```

Output -

![output](https://user-images.githubusercontent.com/86108765/149818293-a68c6644-4bf7-4ae2-ae8e-67abf60e7372.png)

