This Lambda function fetches all EBS snapshots and also it checks the list of active Ec2 instances (running or stopped).
For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. 
If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.