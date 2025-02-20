# CourseCompletionBadge Smart Contract

This smart contract issues NFTs as completion badges for courses or tasks. Each badge is a unique token that is awarded to users upon completion of a course.

## Contract Address
The contract is deployed at: `0xf4ab5aF3757eA564dAb80E2A6E1f85028A90EDbA`

## Functions

### completeCourse(string memory uri)
Allows users to complete the course and receive an NFT badge. Each user can complete the course only once.

- **Parameters**:
  - `uri`: The URI containing metadata or an image link for the badge.

### getOwnedBadges(address owner) view returns (uint256[] memory)
Returns the badge IDs owned by a specific address.

- **Parameters**:
  - `owner`: The address of the owner whose badges you want to query.

### getBadgeURI(uint256 tokenId) view returns (string memory)
Returns the URI of a specific badge by its token ID.

- **Parameters**:
  - `tokenId`: The ID of the badge whose URI you want to query.

## Events

### BadgeMinted(address indexed to, uint256 tokenId, string uri)
Emitted when a new badge is minted.

- **Parameters**:
  - `to`: The address of the recipient.
  - `tokenId`: The ID of the minted badge.
  - `uri`: The URI of the badge.

## Usage

To complete a course and receive a badge:
```solidity
completeCourse("https://example.com/badge/metadata");
