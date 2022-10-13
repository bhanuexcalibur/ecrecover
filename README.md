
# Ecrecover

Signing and verifying message with Solidity.




## Installation

Deploy the solidity code on localhost in Ethereum in remix. Have metamask wallet

```bash
 Make sure to have Metamask or any Ethereum Wallet.
  1.Go to the deployed contract and find a function named "getMessageHash" 
    and enter a string that you want to hash.
  2.Copy the bytes32 output and use that as an input in the another function
    named "ethSignedMessageHash:".
  3.Open console in the browser(Ctrl+Shift+I) and write "ethereum.enable".
    A pop comes up and accept that.
  4."account="your metamask wallet address"". Write this in the console.
  5."hash="The output of getMessageHash"".
    In this line we create two variable and stored the account and hash.
  6.ethereum.request({ method: "personal_sign", params: [account, hash]}).then(console.log)
    This is the way we are signing through Metamask. Metamask pops up and accept it.
  7.Now call a function "recover signer". The first input is _ethSignedMessageHash.
    Copy the output of ethSignedMessageHash and paste it. Second input is signature, 
    get it from the output in the console of your browser.

      Your output will be your address from which you signed.

  8.Now call the function "verify". _signer: "the wallet address", 
    _message: "the message you wrote in the starting", 
    signature: "the output you got in the console". 
  Your output will be true, i.e. it verifies the signature.
If you want to try, change anything in the input of this function, your output will be false.

```
    