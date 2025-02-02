# Utility Processes

## Background writer
Writes dirty data blocks to disk

## WAL writer
Flushes write-ahead log to disk

## Checkpointer
Automatically performs a checkpoint based on config parameters

## Autovacuum launcher
Starts Autovacuum workers as needed

## Autovacuum workers
Recover free space for reuse

## Logging collector
Routes log messages to syslog, eventlog, or log files

## Stats collector
Collects usage statistics by relation and block

## Archiver
Archives write-ahead log files

## Logical replication launcher
Starts logical replication apply process for logical replication

## Dbms_aq launcher
Collects information for queueing functionality of advanced server
