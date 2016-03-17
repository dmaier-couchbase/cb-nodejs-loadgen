# cb-nodejs-loadgen
A node based load generator for Couchbase


# Requirements

We keep the tool simple and stupid. Multiple threads and workload patterns can be reached by starting multiple instances of the tool.

## Connections
* Connect with user name and password to a bucket
* The password is optional

## Load pattern
* Define if it is a create, update or read workload
* Define the key range on which the workload should be performed
* Define how many operations should be performed

## JSON document database requirement
* Create/update JSON documents based on a template file
* Work on documents with a specific document prefix

# Implementation ideax

```
loadgen {--host=$host} {--bucket=$bucket} [--password=$password] [--prefix=$prefix] {--range_min=$min} {--range_min=$max} {--workload=[create|update|read]}  {--num_ops=$num} {--template=$template_file}
```
