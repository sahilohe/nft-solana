# buildspace Solana NFT Drop Project
### Welcome 👋
#### Sorry guys, the code is not updated! Don't use my code in your project files! follow the project notes.

## Metaplex error fix

clone the metaplex repo `git clone https://github.com/metaplex-foundation/metaplex.git`
run `sudo yarn install --cwd ~/metaplex/js/` (I'm working on WSL2)
then run `ts-node ~/metaplex/js/packages/cli/src/candy-machine-v2-cli.ts --version`. this command should spit out `0.0.2`

make sure that all your assests and .config files are all correct

run this command `ts-node ~/metaplex/js/packages/cli/src/candy-machine-v2-cli.ts upload -e devnet -k ~/.config/solana/devnet.json -cp config.json ./assets`
from the root of the project folder, where you have put the assests folder.

you will set similar result 

`wallet public key: A1AfJpXEiqiP3twp6CdZCWixpyx6p8E26zej4TNQ12GT
WARNING: The "arweave" storage option will be going away soon. Please migrate to arweave-bundle or arweave-sol for mainnet.

Beginning the upload for 3 (img+json) pairs
started at: 1641470635118
Size 3 { mediaExt: '.png', index: '0' }
Processing asset: 0
initializing candy machine
initialized config for a candy machine with publickey: 5FUh6tm4sATuCA6hth9a4JAuko9GEAhsewULrXa5zS8C
Processing asset: 0
Processing asset: 1
Processing asset: 2
Writing indices 0-2
Done. Successful = true.
ended at: 2022-01-06T12:04:38.862Z. time taken: 00:00:43`

then run this command  `ts-node ~/metaplex/js/packages/cli/src/candy-machine-v2-cli.ts verify_upload -e devnet -k ~/.config/solana/devnet.json` to verify your nfts are uploaded or not

that's it! the rest works! follow up the project notes properly!
