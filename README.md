# globusT

Having a simple command-line script that can interact with Globus, similar to s3cmd for s3, would be pretty useful. The ssh CLI is useful, but it is not available on some clusters because of firewalls. Being able to use a REST-based client would be helpful in the situation that an http proxy is available.  

I would propose using one of the language bindings, such as python, to build a minimal command-line tool for performing common tasks.

## Proposal

Would take globus endpoint/paths as URIs.

- globust scp (with flag for async or synchronous)
  - Transfer, basically like scp
  - async transfer returns task id
- globust ls
  - list an endpoint directory
- globus sync (with flag for async or synchronous)
  - like rsync
  - async rsync returns task id
- globust task TASKID
  - return status information about the transfer task where TASKID comes from globust transfer
- globust cancel TASKID
