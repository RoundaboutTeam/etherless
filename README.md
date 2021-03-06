# Etherless
Etherless is a Cloud Application Platform which allows developers to deploy Javascript functions in the cloud and let pay final users for their execution, by leveraging the Ethereum's smart contract technology.

# Installation 
- Download this repo.
- From inside of the etherless sub-modules run the command <code>npm install</code> to install all the missing dependecies.

# Commands 
To use a command from inside the repository run: <code>etherless `<command>` [params...]</code>

## Init 
Command: <code>etherless init</code> <br/> 
The init command shows a brief introduction to the Etherless-cli module. 

## Signup 
Command: <code>etherless signup [--save]</code> <br/> 
Will create an Ethereum account for you, and show its: address, private key and mnemonic phrase. You can request to save these informations inside a file of the current directory with the flag <code>--save</code>.

## Login 
### Login with private key 
Command: <code>etherless login `<private_key>` </code> <br />
It will log the user in an Ethereum wallet with the private key inserted. <br>
A password to encrypt the wallet will be requested after executing this command.
### Login with mnemonic phrase 
Command: <code>etherless login -m `<mnemonic_phrase>` </code> <br />
It will log the user in an Ethereum wallet with the mnemonich phrase you inserted. <br>
A password to encrypt the wallet will be requested after executing this command.

## Logout 
Command: <code>etherless logout</code> <br />
After executing this command all the saved credentials will be deleted. 

## List 
### List all functions
Command: <code>etherless list</code> <br />
After executing this command a list of all functions available in the platform will be shown.
### List owned functions 
Command: <code>etherless list -m</code> <br />
After executing this command a list of all functions owned by the current user will be shown.
  
## Info 
Command: <code>etherless info `<function_name>`</code> <br />
After executing this command, all details about the functioin will be shown. 
  
## Run 
Command: <code>etherless run `<function_name>` [params...]</code> <br />
After executing this command, the function result will be shown. 
  
## Deploy 
Command: <code>etherless deploy `<function_name>` `<source_path>` `<description>`</code> <br />
After executing this command a success or error message will be shown. The "source_path" parameter can be:
 - a directory, if your function has dependencies. The directory must contain the following files: index.js, package.json and package_lock.json
 - a javascript file, if your function has no dependencies
  
## Delete 
Command: <code>etherless delete `<function_name>`</code> <br />
After executing this command the considered function will be deleted 

## History 
Command: <code>etherless history [--limit]</code> <br />
Following the execution of this command, a list of the user's past execution requests will be shown, with the relative results. The limit parameter indicates the maximum number of elements in this list.

## Search 
Command: <code>etherless search `<keyword>` </code> <br />
A list of all functions containing the "keyword" parameter inside their name will be shown. 

## Whoami 
Command: <code>etherless whoami</code> <br />
If there is a user logged inside the Etherless-cli module, his address will be shown. 
