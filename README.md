# globusT

## Proposal

- globust scp 
  - Synchronous transfer, basically like scp
- globust ls
  - list an endpoint directory
- globust transfer
  - async transfer, returns task ID
- globust task TASKID
  - return status information about the transfer task where TASKID comes from globust transfer
- globust cancel TASKID
