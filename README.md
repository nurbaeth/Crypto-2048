# Crypto 2048

Crypto 2048 is a decentralized version of the classic 2048 game implemented as a smart contract on the Ethereum blockchain. Players can interact with the contract to make moves, track their scores, and compete for the highest ranking on-chain.

## Features
- **Fully On-Chain Gameplay**: All game logic is executed on the blockchain.
- **Immutable Score Tracking**: Your highest score is recorded permanently.
- **Decentralized & Transparent**: Anyone can verify the game state at any time.
- **Future Expansion**: Potential integration with token rewards or NFTs.    

## How It Works 
1. **Start a Game**: Call the `startGame()` function to initialize the board.
2. **Make Moves**: Use `makeMove(direction)` to shift the board (0 = up, 1 = right, 2 = down, 3 = left).
3. **Score Calculation**: The contract keeps track of your score as you merge tiles. 
4. **Game Over**: If no moves are available, the game ends, and your highest score is recorded.  

## Smart Contract Overview   
- **`startGame()`**: Initializes a new game session for the player.
- **`makeMove(uint8 direction)`**: Moves tiles in the specified direction.
- **`highScores(address player)`**: Retrieves the highest score of a given player.
- **Events**:
  - `GameStarted(address player)` – Triggered when a new game starts. 
  - `MoveMade(address player, uint256 newScore)` – Triggered after a move.
  - `GameOver(address player, uint256 finalScore)` – Triggered when the game ends.
 
## Deployment
This contract is designed for Ethereum-compatible blockchains like Ethereum, Polygon, or Arbitrum. Use Hardhat or Remix to deploy and interact with it.

## Future Improvements
- Implement full board movement logic.
- Add off-chain front-end integration.
- Introduce token-based incentives for top players.

## License
This project is released under the MIT License.
