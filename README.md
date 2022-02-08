# Oaswap Subgraph

TheGraph exposes a GraphQL endpoint to query the events and entities within the Oasis Emerald ParaTime and Oaswap ecosystem.

Currently, there are multiple subgraphs, but additional subgraphs can be added to this repository, following the current architecture.

## Subgraphs

1. **[Blocks](https://thegraph.com/legacy-explorer/subgraph/oaswap/blocks)**: Tracks all blocks on the Oasis Emerald ParaTime.

2. **[Exchange](https://oaswap.medium.com/oaswap-info-relaunch-in-partnership-with-150-000-bounty-winner-streamingfast-f7892559d388)**: Tracks all Oaswap Exchange data with price, volume, liquidity, ...

6. **[Pairs](https://thegraph.com/legacy-explorer/subgraph/oaswap/pairs)**: Tracks all Oaswap Pairs and Tokens.

## Dependencies

- [Graph CLI](https://github.com/graphprotocol/graph-cli)
    - Required to generate and build local GraphQL dependencies.

```shell
yarn global add @graphprotocol/graph-cli
```

## Deployment

For any of the subgraph: `blocks` as `[subgraph]`

1. Run the `cd subgraphs/[subgraph]` command to move to the subgraph directory.

2. Run the `yarn codegen` command to prepare the TypeScript sources for the GraphQL (generated/*).

3. Run the `yarn build` command to build the subgraph, and check compilation errors before deploying.

4. Run `graph auth --product hosted-service '<ACCESS_TOKEN>'`

5. Deploy via `yarn deploy`.
