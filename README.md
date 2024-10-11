# High-level python interface to the AWS Neptune graph database

`NeptuneAccess` is a port to AWS Neptune of the Neo4j-based `NeoAccess` library, with is part of the open-source project [BrainAnnex.org](https://BrainAnnex.org)

For general information about motivation and usage for this library, please see:

[Intro and tutorial](https://julianspolymathexplorations.blogspot.com/2023/06/neo4j-python-neoaccess-library.html)


### Notes:


## Graph Query Languages:
- **Property Graphs**: Gremlin
- **RDF**: SPARQL

## Advantages in Healthcare:
Graph databases excel in managing the complexity of healthcare data due to:
- Continuous research and development of drugs and medicines
- Numerous data types and complex relationships between them

## Leading Graph Models:
1. **Property Graphs**
   - Frameworks: TinkerPop
   
2. **Resource Distribution Framework (RDF)**


## Compatibility with BrainAnnex with Neptune:
- Successfully migrated all methods for interacting with AWS Neptune
- Remaining tasks related to indexing and constraints in Neptune

## Insights from Migration:

1. **APOC Fix**
   - Unable to use APOC library due to Neptune limitations
   - Modified routines to bypass APOC calls
   
2. **Indexing in AWS Neptune**
   - Neptune does not support Cypher for index creation
   - Methods for manual and automatic indexing in Neptune
   
3. **Constraints in Neptune**
   - Alternative approaches for data constraints in Neptune
   - Schema validation, query-based validation, and graph-level constraints
   
4. **Neptune vs. Neo4j Migration Compatibility**
   - Considerations for migrating between Neptune and Neo4j
   
5. **Internal IDs in Neptune and Neo4j**
   - Internal IDs not guaranteed to be consistent across sessions
   - Recommendations for reliable node identification

# Neptune vs. Neo4j: Key Differences

## Deployment:
- Neptune: Managed service on AWS
- Neo4j: Self-hosted or cloud-based options

## Integration:
- Neptune: Tight integration with AWS services
- Neo4j: Integration with various cloud platforms

## Query Language:
- Neptune: Supports Gremlin and SPARQL
- Neo4j: Uses Cypher language

## Data Consistency:
- Neptune: Eventual consistency model
- Neo4j: Strong consistency guarantees

## Support & Community:
- Neptune: Growing community, support through AWS documentation
- Neo4j: Large community, extensive documentation, dedicated support

## Other Differences:
- APOC Support, Indexing, Constraints, Cost

## Choosing the Right Option:
- Neptune: Tight AWS integration, eventual consistency
- Neo4j: User-friendly interface, strong consistency, active community support


## To test the testcases:
   
   export NEPTUNE_HOST=<neptune_host>
   
   pytest tests/test_neptuneaccess.py -vv
