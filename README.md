# IronFinanceV2Compounder
for https://app.iron.finance
**onlyOwner compounding contract for the IronSwap IS3USD stablecoin LP farm**
- Note: unaudited. transferOwnership not possible.

input `0` for the '\_pid' upon deployment to access the IS3USD IronChef farm.

compound() function - harvests ICE rewards, swaps for USDC, deposits USDC into IronSwap for IS3USD, and then finally deposits the IS3USD tokens into the farm. Simple compounder without any advanced strategies.

depositToIron() function - deposit any IS3USD tokens in the contract.

emergencyWithdrawFromIronONCE() function - withdraw all your IS3USD and ICE rewards to the owner/deployer address from Iron. Can only be called once. Do not use or deposit anything into this deployed contract again, create another one.

withdrawTokensFromContract() function - withdraw any ERC20 token that happens to be in the contract.

call() - in case of an emergency, this function allows the owner to interact with any other contract through this contract.

not responsible for any losses if anyone actually uses this lmao.
