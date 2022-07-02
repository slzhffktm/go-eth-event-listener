# Running The Go Event Listener

This is following the [goethereumbook.org Reading Event Logs tutorial](https://goethereumbook.org/event-read).

## Getting Started

1. Make sure you have `go` installed. This tutorial is using `go 1.18`
2. Copy the `.env.example` file to `.env` and fill in the values, 
   where the `CONTRACT_ADDRESS` is the address from the `contracts/.env`
3. Run `make start` to start the event listener
4. You should see the `Listening to events...` in the terminal

## Testing the Event Listener

1. Make sure that the event listener is running
2. Go to the `contract/` directory and follow the [Interacting with The Deployed Smart Contract](../contracts/README.md#Interacting with The Deployed Smart Contract)
3. You should see the event being logged in the terminal
