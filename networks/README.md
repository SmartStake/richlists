# Networks
A repository for managing known addresses for Networks. Data stored in this repository is used to build the network native coin richlists at https://analytics.smartstake.io

# Instructions to add known addresses or IBC assets for a network/chain

Precheck:
 1. Confirm that Smart Stake supports the network. SmartStake.io lists all supported networks.

Instructions:
 1. Fork this repository
 2. In your own instance of the repository, check to see if NetworkSymbol.json file is present (e.g. INJ.json)
 3. Create NetworkSymbol.json file (e.g. INJ.json) with below structure and enter all the information that is available. The JSON file has below given structure (see sample values & explanation). Please pay attention to the case of attributes (e.g. logoUrl is the correct attribute logourl and LOGOURL are wrong). Also note that the full structure must be present, if you dont have some of the information, you can leave that as null (without any double quotes)
 
```   
{
    "network": "INJ", # mandatory - ticker for the network where the token is minted
    "knownAddresses": [
        {
            "address": "inj1nyu6sk9rvtvsltm7tjjrp6rlavnm3e4sq03kltde6kesam260f8szar8ze",
            "alias": "Astroport Staking"
        },
    ],
    "ibc": [ # listing of IBC assets for this network e.g if network is present as ibc asset in OSMO, LUNA, below entries are needed
        {"network": "OSMO", "denom": "ibc/42A9553A7770F3D7B62F3A82AF04E7719B4FD6EAF31BE5645092AAC4A6C2201D", "knownAddresses": [
            {"address": "osmo1nyu6sk9rvtvsltm7tjjrp6rlavnm3e4sq03kltde6kesam260f8szar8ze", "alias": "Astroport Staking"}]},
        {"network": "LUNA", "denom": "ibc/0EC78B75D318EA0AAB6160A12AEE8F3C7FEA3CFEAD001A3B103E11914709F4CE", "knownAddresses": []}
    ],
}
```
 4. Commit changes to your branch
 5. Open a pull request
 6. In case of delays in your changes getting accepted/rejected (give it 1 business day), reach out to Smart Stake support at https://t.me/SmartStake or https://t.me/bigb4ever
 7. After pull requested is accepted, give it another 4 hours before checking richlist on https://analytics.smartstake.io. If richlist still doesn't appear, reach out to Smart Stake support.
