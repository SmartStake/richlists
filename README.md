# Tokens
A repository for managing token richlists. Data stored in this repository is used to build the tokens richlists at https://analytics.smartstake.io

The listing of any tokens on smart stake is not an endorsement for the token. This is currently a free service for all the tokens. If you like to support Smart Stake, consider staking with Smart Stake and/or encouraging your communities to stake with Smart Stake.


# Instructions to add a new token

Prechecks:
 1. Confirm that Smart Stake supports the network on which you have launched the token. SmartStake.io lists all supported networks.
 2. Confirm that the token being requested for listing is a token factory token

Instructions:
 1. Fork this repository
 2. In your own instance of the repository, check to see if TokenSymbol.json file is present (e.g. BULLS.json)
 3. Create TokenSymbol.json file (e.g. BULLS.json) with below structure and enter all the information that is available. The JSON file has below given structure (see sample values & explanation). Please pay attention to the case of attributes (e.g. logoUrl is the correct attribute logourl and LOGOURL are wrong). Also note that the full structure must be present, if you dont have some of the information, you can leave that as null (without any double quotes)
 
```   
{
    "name": "Alpha Bulls", # mandatory (the comments mentioned here should not be added to the json file you submit. see any of the existing file for reference)
    "ticker": "BULLS", # mandatory
    "network": "INJ", # mandatory - ticker for the network where the token is minted
    "tokenType": "tokenfactory", # mandatory - tokenfactory or ibc or smartcontract
    "tokenDenom": "factory/inj1zq37mfquqgud2uqemqdkyv36gdstkxl27pj5e3/bulls",  # mandatory for tokenfactory or ibc. must match the format given. Try total supply API for the network to figure out the correct input e.g. https://rest.cosmos.directory/injective/cosmos/bank/v1beta1/supply. For token factory tokens, it will be like: factory/inj1zq37mfquqgud2uqemqdkyv36gdstkxl27pj5e3/bulls. For an IBC asset, it will be like: ibc/0EC78B75D318EA0AAB6160A12AEE8F3C7FEA3CFEAD001A3B103E11914709F4CE
    "holderContract": null, # mandatory for smartcontract based tokens
    "stakerContract": null, # optional and applicable only for smartcontract based tokens at this time
    "exponent": 6, # mandatory. number of decimal places in the token balance
    "description": "Curated Alpha information for community", # optional value. not needed for IBC assets if they are already supported on smart stake on the primary network e.g. Terra for Astroport
    "logoUrl": "https://ibb.co/hD0YvBf", # mandatory for tokenfactory. not needed for IBC assets 
    "website": "https://www.alphabulls.xyz", # optional value. not needed for IBC assets
    "twitter": "Alphabulls_", # optional value. twitter handle is enough. not needed for IBC assets
    "telegram": null, # optional value. tg handle is enough. not needed for IBC assets
    "telegram2": null, # optional value. tg handle is enough. not needed for IBC assets
    "discord": "https://discord.gg/wmt9c5F2Ex", # optional value. share full value of the url. not needed for IBC assets
    "coingeckoId": null, # optional value (update it when it becomes available) - API Id from coingecko.com. This will be used to show dollar value of token balances. not needed for IBC assets
    "status": "active" # mandatory. Active indicates token is to be supported. Inactive or any other value will delist the token from Smart Stake
    "knownAddresses": [
        {"inj1a78hlc49t4g3xls4zm0f59aqqvnq7d7c6reaa6": "Astroport LP"},
        {"xxxx": "DAO"},
        {"xxxx": "Airdrop"}
    ],
    "ibc": [ # listing of IBC assets for this token e.g if token is present as ibc asset in OSMO, INJ, SEI, below entries are needed
        {"network": "OSMO", "denom": "ibc/42A9553A7770F3D7B62F3A82AF04E7719B4FD6EAF31BE5645092AAC4A6C2201D", "knownAddresses": []},
        {"network": "INJ", "denom": "ibc/EBD5A24C554198EBAF44979C5B4D2C2D312E6EBAB71962C92F735499C7575839", "knownAddresses": []},
        {"network": "SEI", "denom": "ibc/0EC78B75D318EA0AAB6160A12AEE8F3C7FEA3CFEAD001A3B103E11914709F4CE", "knownAddresses": []}
    ],
}
```
 4. Commit changes to your branch
 5. Open a pull request
 6. In case of delays in your changes getting accepted/rejected (give it 1 business day), reach out to Smart Stake support at https://t.me/SmartStake or https://t.me/bigb4ever
 7. After pull requested is accepted, give it another 4 hours before checking richlist on https://analytics.smartstake.io. If richlist still doesn't appear, reach out to Smart Stake support.


# Instructions to update a token
 1. re-sync your fork of the repository from the master branch
 2. make changes as necessary
 3. Commit changes to your branch
 4. Open a pull request
 5. In case of delays in your changes getting accepted/rejected (give it 1 business day), reach out to Smart Stake support at https://t.me/SmartStake or https://t.me/bigb4ever
 6. After pull requested is accepted, give it another 4 hours before checking richlist on https://analytics.smartstake.io. If richlist doesn't reflect your changes, reach out to Smart Stake support.


# Instructions to delete a token
 1. re-sync your fork of the repository from the master branch
 2. delete the token file
 3. Commit changes to your branch
 4. Open a pull request
 5. In case of delays in your changes getting accepted/rejected (give it 1 business day), reach out to Smart Stake support at https://t.me/SmartStake or https://t.me/bigb4ever
 6. After pull requested is accepted, the token will be removed from the richlist manually.
