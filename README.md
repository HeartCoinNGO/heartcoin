# HeartCoin Token (HCO)
ERC721 token public smart contract repository.

http://www.heartcoin.ong/#token

## Contract

The contract is in `HeartCoin.sol`. It is the solidity of the implementation contract.

The HCO contract is based upon the Non-Fungible Token Standard.

## Contract Specification

HeartCoin (HCO) is an ERC721 token that is created by Fundación HeartCoin. 

### ERC721 Token

The public interface of HeartCoin Token is the ERC721 interface
specified by [EIP-721](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-721.md).

- `name()`
- `symbol()`
- `decimals()`
- `totalSupply()`
- `balanceOf(address who)`
- `transfer(address to, uint256 value)`
- `approve(address spender, uint256 value)`
- `allowance(address owner, address spender)`
- `transferFrom(address from, address to, uint256 value)`

And the usual events.

- `event Transfer(address indexed from, address indexed to, uint256 value)`
- `event Approval(address indexed owner, address indexed spender, uint256 value)`

Typical interaction with the contract will use `transfer` to move the token as payment.
Additionally, a pattern involving `approve` and `transferFrom` can be used to allow another 
address to move tokens from your address to a third party without the need for the middleperson 
to custody the tokens, such as in the 0x protocol. 

## Contract Tests

To run smart contract tests first start 

`ganache-cli`

in another terminal

Then run 

`make test-contracts`

You can also run `make test-contracts-coverage` to see a coverage report.