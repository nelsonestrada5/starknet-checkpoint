### What is Checkpoint
Checkpoint is a library for indexing data from StarkNet events and making it accessible through GraphQL. It provides similar functionality to The Graph but for StarkNet. Checkpoint performs two main functionalities:

1. Indexing contract data based on StarkNet events
2. Exposes a GraphQL API to query this data.

### How it works
Checkpoint learns what and how to index StarkNet data based on configuration parameters and user-defined JavaScript functions called Data Writers.

The configuration parameters define the smart contract addresses of interest and the relevant events Checkpoint should be tracking. The Data Writers describe the logic that maps events to data that Checkpoint will store in its database. Checkpoint then exposes the stored data to the public through a GraphQL API.

This diagram shows the flow of data once a Checkpoint instance has started processing StarkNet transactions:

![image](https://user-images.githubusercontent.com/8497284/173718143-b88ec19c-9cf0-4722-a24b-a1e7c8b26d91.png)
