<!-- 
Document for Medium MongoDB API updates
-->

## March 2022 Updates

### Use nameof(MongoNativeRbacControlPlaneUtilities) for FabricClient
Minor change to use the standard approach of utilizing the nameof expression for the component name when creating a fabric client facade.

### Bump System.runtime.compilerservices.unsafe to 6.0.0.
This is a base line dependency that every other package tends to depend on.
As part of this bump a few projects to .net 6.0 and clean up any version overrides.

### Add support for ping request for SCRAM-SHA-256
Using SCRAM-SHA-256 auth with mongosh results in the error "command ping not supported". Adding support for ping request in PostgresMongoRequestHandler.

### Add system user configuration for config/auth calls
In test pipelines we already set this to make it run cross-user. however, in prod, we were initially running the pg process as the same user (earlier), but switched to a dedicated linux user for the GW. After that change, we need to have a user mapping to make calls to the GW for system calls. Matching the behavior we have in test with prod.

