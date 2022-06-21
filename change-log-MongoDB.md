<!-- 
Document for Medium MongoDB API updates
-->

### Transaction commands
> [!NOTE]
> Multi-document transactions are only supported within a single non-sharded collection. Cross-collection and cross-shard multi-document transactions are not yet supported in the API for MongoDB.

| Command | Supported |
|---------|---------|
| abortTransaction | Yes |
| commitTransaction | Yes |
