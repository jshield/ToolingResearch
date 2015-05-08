# Database Change Tracking

_Data Schema as Source Code_

 * Track Changes made to Schema
    * Database to Database Diff?
    * Source to Database Diff?
    * Database to Source Diff?
 * Multiple Developers/Branches
    * Tracking Unique Ids for Changesets
        * Distribute from a central authority?
        * Create based on Developer and Time?
    * Conflicting Changesets?
        *  Diff/Merge Tooling?
    *  Distributing Changes to developers on commit?
        * SCM Hooks?   
 * Feature Support
    * Only basic DDL Statements?
    * What about Views, SPs, Indices? 
 * Database Support?
    * Avoid Tools that are Single Database Engine only
    * Only SQL RDBMS Engines? NoSQL? 
 * Programming Language agnostic
 * SCM Integration (Git, TFS)
    * Avoid having to maintain two SCM tools
 * Application Database version identification?
    * How to determine whether the database implements all the requisite data structures for a given DAL?
        * Version Numbers?
        * Feature Numbers?
        * Timestamps?
        * Hashes?
    * Schema Versioning similar to API versioning?
        *  a given version number is guaranteed to support all the features required?
        *  How to support multiple versions in the same database?
            * Views?
            * Translation Service Layer?
            * Oracle Edition Based Redefinition?

## Reading Material
 * http://martinfowler.com/articles/evodb.html
 * http://www.liquibase.org/
 * http://sqitch.org/
 * http://en.wikipedia.org/wiki/Schema_migration