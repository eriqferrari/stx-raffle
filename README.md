STX RAFFLE

The STX Raffle is an innovative on-chain raffle system built on the Stacks
blockchain, offering a secure and transparent mechanism for organizing raffles
with unpredictable randomness. This contract supports three types of raffles:
STX, fungible tokens (FT), and non-fungible tokens (NFT). Participants can
enjoy a fair and trustless raffle experience where the creator receives the
collected funds and the winner receives the prize.
 
Key features include the ability to set a maximum ticket limit per wallet,
ensuring fair participation. For FT and NFT raffles, tickets can be offered  for
free, with users only covering the transaction fees. The randomness is  derived
from a combination of the block Header ID Hash, the timestamp, and  the raffle's
name hash, creating a robust source of entropy.
 
The draw function works by first generating a keccak256 hash of the raffle's
name. This name hash is then combined with the timestamp and hashed again  using
keccak256. The resulting hash is further combined with the block Header  ID Hash
and hashed once more using keccak256, like this: keccak256(id header +
keccak256(timestamp + keccak256(name))). This process  produces a final hash
that is used to determine the winner, ensuring a high  level of unpredictability
and security in the raffle outcome.
 
The draw function is a read-only function, allowing anyone to verify the
results of the raffle at any time without incurring any costs. This function  is
crucial for maintaining transparency and fairness, as participants can
independently confirm the outcome of the raffle without relying on third
parties.  The read-only nature ensures that the function is accessible and
cost-free,  encouraging broader participation in the verification process.
 
Additionally, the function responsible for sending the prize is public, meaning
that any participant or observer can trigger it. This design choice reinforces
the decentralized nature of the contract, ensuring that the prize distribution
is open and transparent. By allowing anyone to trigger the prize distribution,
the contract minimizes the risk of centralized control or manipulation.
 
This on-chain randomness is both transparent and verifiable, providing all
participants with confidence in the fairness of the raffle process. The raffle
operates without a predefined time limit, allowing the draw to be triggered
only after all tickets are sold. This ensures that the raffle progresses  fairly
and that the draw can only occur once the participation criteria are  fully met.
This feature provides participants with certainty that the raffle  will only
conclude when all tickets are accounted for, further enhancing the  overall
transparency and fairness of the system.
 
In terms of functionality, the contract is designed to be user-friendly and
accessible, with clear parameters for entering and managing raffles. Users  can
easily participate in raffles using STX to purchase tickets, with  the entire
process being managed on-chain to ensure full transparency. The  use of
blockchain technology guarantees that every step of the raffle, from  ticket
purchase to winner selection, is recorded and cannot be altered or  tampered
with.
 
This contract leverages the power of Stacks to deliver a fully decentralized,
transparent, and secure raffle experience. Users can rest assured that the
randomness and the process as a whole are immune to manipulation, providing  a
trustworthy and enjoyable platform for decentralized raffles. Furthermore,  the
combination of multiple sources of randomness, along with the public draw
function, establishes a robust system where fairness is at the forefront of
every raffle.
 
The STX Raffle represents a new era in decentralized gaming and fundraising,
offering users a reliable and transparent way to engage in raffles. Whether  for
entertainment, charity, or other purposes, this contract ensures that  every
participant has a fair chance to win, with the entire process being  open to
scrutiny and verification by anyone with access to the blockchain.
