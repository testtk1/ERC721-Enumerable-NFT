# ERC721-Enumerable-NFT
ERC721 Enumerable NFT
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC721/extensions/ERC721Enumerable.sol";

contract EnumNFT is ERC721Enumerable {
    uint256 public nextId;

    constructor() ERC721("EnumNFT", "ENFT") {}

    function mint() public {
        _mint(msg.sender, nextId++);
    }
}
