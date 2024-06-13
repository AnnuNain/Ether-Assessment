MyToken Contract

Variables:
tokenName: token name (e.g. "AnnuNain")
tokenAbbrv: token abbreviation (e.g. "AN")
totalSupply: total supply of tokens
balances: mapping of addresses to their token balances

Modifier: hasSufficientBalance(address _address, uint _amount)  :-
     Checks if _address has at least _amount tokens in their balance before executing the burn().
     Reverts the transaction if the balance is insufficient with a error message 'Insufficient Balance'.

Features:
Minting: allows authorized addresses to create new tokens
Burning: allows authorized addresses to destroy existing tokens
Balance tracking: keeps track of the total supply and individual balances of tokens
Modifier: checks if an address has sufficient balance before allowing a burn operation


Functions:
mint(address _address, uint _amount) : Mints _amount new tokens and assigns them to _address And also Increases the total supply by _amount
burn(address _address, uint _amount):  Burns _amount tokens from _address. Also Decreases the total supply by _amount. Also,Requires the hasSufficientBalance modifier to ensure the address has enough tokens to burn


Deploy and test: Compile and deploy to your preferred Ethereum network using Truffle or Remix.


