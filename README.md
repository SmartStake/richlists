# Tokens
A repository for managing token richlists. Data stored in this repository is used to build the tokens richlists at https://analytics.smartstake.io

The listing of any tokens on smart stake is not an endorsement for the token. This is currently a free service for all the tokens. If you like to support Smart Stake, consider staking with Smart Stake and/or encouraging your communities to stake with Smart Stake.


# Instructions to add a new token

Prechecks:
 1. Confirm that Smart Stake supports the network on which you have launched the token. SmartStake.io lists all supported networks.
 2. Confirm that the token being requested for listing is a token factory token

Instructions:
 1. Fork this repository
 2. In your own instance of the repository, check to see if TokenSymbol-Network.json file is present (e.g. BULLS-INJ.json)
 3. Create TokenSymbol-Network.json file (e.g. BULLS-INJ.json) with below structure and enter all the information that is available (e.g. AUTISM.json). The JSON file has below given structure (see sample values & explanation). Please pay attention to the case of attributes (e.g. logoUrl is the correct attribute logourl and LOGOURL are wrong). Also note that the full structure must be present, if you dont have some of the information, you can leave that as null (without any double quotes)
 
```   
{
    "ticker": "BULLS", # mandatory
    "network": "INJ", # mandatory - ticker for the network where the token is minted
    "tokenFactoryDenom": "factory/inj1zq37mfquqgud2uqemqdkyv36gdstkxl27pj5e3/bulls",  # mandatory. must match the format given
    "exponent": 6, # mandatory. number of decimal places in the token balance
    "name": "Alpha Bulls", # mandatory
    "description": "Curated Alpha information for community", # optional value
    "logoUrl": "https://ibb.co/hD0YvBf", # mandatory
    "website": "https://www.alphabulls.xyz", # optional value
    "twitter": "Alphabulls_", # optional value. twitter handle is enough.
    "telegram": null, # optional value. tg handle is enough.
    "telegram2": null, # optional value. tg handle is enough.
    "discord": "https://discord.gg/wmt9c5F2Ex", # optional value. share full value of the url
    "coingeckoId": null, # optional value (update it when it becomes available) - API Id from coingecko.com. This will be used to show dollar value of token balances.
    "knownAddresses": [
        {"inj1a78hlc49t4g3xls4zm0f59aqqvnq7d7c6reaa6": "Astroport LP"},
        {"xxxx": "DAO"},
        {"xxxx": "Airdrop"}
    ]
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
