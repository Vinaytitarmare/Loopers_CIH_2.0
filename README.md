# 🎟️ EventureNFT - On-Chain Event Ticketing with NFTs

Eventure is a decentralized platform for event ticketing built on the Ethereum blockchain using smart contracts. Each ticket is a unique ERC-721 NFT, offering transparency, traceability, and security for both event organizers and attendees.

---

## 📸 Project Preview

![image](https://github.com/user-attachments/assets/ed10236f-fc6b-4e38-8391-8a9a4330a944)


---

## 🚀 Features

- ✅ **Create Events**: Organizers can create events with a maximum ticket limit and metadata stored via IPFS.
- 🎟️ **Mint Tickets**: Users can mint tickets as NFTs tied to a specific event.
- 🔄 **Resale Support**: Tickets can be listed and resold at a user-defined price.
- ❌ **Cancel Events**: Organizers can cancel events and potentially refund ticket holders.
- 🔒 **Secure & Transparent**: On-chain logic ensures tamper-proof records and fair validation.

---

## 🧠 Smart Contract Architecture

Built with **Solidity** and **OpenZeppelin** contracts:
- **ERC721URIStorage** for minting NFTs with metadata
- **Ownable** for admin and organizer control
- **Structs & Mappings** to manage events, ticket ownership, resale, and metadata

```solidity
struct Event {
    address organizer;
    string metadataHash;
    uint256 maxTickets;
    uint256 soldCount;
    bool isCancelled;
    bool exists;
}
