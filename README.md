<h1> Ethereum Mint-Bot </h1>

This is one if not the fastest mint bot out there, you'll be able to mint NFTs as soon as the mint starts. The system is really optimized and you should be able to win any gas war for you're hyped mints.


<h2> Setup </h2> 

> Download the latest release via github.

Open then the Config.json file and start changing strings:

```json
{
    "APIs": {
        "node": "Your node provider here. (alchemy, infura or any private)",
        "BlockNative": "Grab your blocknative api key at https://blocknative.com/",
        "Etherscan": "Get an etherescan API key on their official website, create an account and navigate to the API selection, create a new code and put it here."
    },
    "Wallet": {
        "privateKey": "Put here your private key",
        "PublicAddress": "Put here your public address (the one people send funds to) this is a security check to see if the public and private key match."
    },
    "Minting": {
        "GasMultiplier": "Put here the gas multiplier, I would use 1.5",
        "MaxReverts": "Max reverts before exit",
        "mintableContract": "Contract address",
        "MintFunction": "Function where you mint with",
        "Mints": "You're max mints",
        "MintPrice": "Mint price in ETH",
        "MintsPerTx": "Max mints per tx"
    },
    "Discord": {
        "Webhook": "Discord webhook URL"
    }
}
```

After changing them **ALL** and set them to personal data you can proceed opening the file and start the executable. It'll probably log that it's estimating gas limit, and that it's calculating the GWEI that would be needed to make the transaction work.

As soon as the calculation is done it'll either log the transaction (etherscan link) or it'll say reverted and it'll loop till it's not reverted. (As soon as it can mint, it'll mint)
