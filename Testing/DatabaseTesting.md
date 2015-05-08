# Database Testing

 * Restoring Consistency after Test Run
    * Snapshot and Restore
        * Spotty support in most RDBMS (i.e. not really) or only in Enterprisey Editions (SQL Server) 
    * Backup and Restore
        * Slow?
    * New Database every test run
        * Keeps artifacts after test run for inspection/reporting
        * Storage Consumption (How to automatically prune?)
 * Speed of Test Run
    * Databases are typically file I/O heavy.
        * SQLite?
        * SQL Server 2014's In Memory OLTP
        * Create Database on a RAM Disk
        * In Memory Provider of Data Access Framework
 * Concurrency Issues with Parallel Database Tests
    * Database Instance Isolation?
    * Write Tests in a manner so that they co-operate? 
        * Bahahahahaha
    * Don't?
 * Local Developer Testing needs instance of database engine installed
    * Virtual Machines
        * Storage/RAM Limited? 
        * Automation Issues with Hyper-V/VMware (Vagrant?)
    * Cloud Database Instances 
        * Bandwidth Limited? 
        * Azure: Easy enough to create/destroy SQL server instances programmatically
    * Local install on Developer Machine
        * Pain in the arse to manage? 
        * Feature Differences between Developer and Production Editions?
 * Generation of Test Data
    * Data Generation Tools (Red Gate)
        * Data be realistic or approximal?
        * Speed of Generation?
    * Fuzzer Tools for finding problems with constraints
    * Load testing
        * Synthesising Realistic User Data Behaviour ("Bots"???)
        * Part of Database Testing Scope???