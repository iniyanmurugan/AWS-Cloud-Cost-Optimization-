AWS Cloud Cost Optimization using boto3(Python) and Lambda function(AWS)
Identifying Stale EBS Snapshots
In this example, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

Description:
Paste the EBS code into a Lambda function and give IAM permissions to it, as it is using other AWS services. 
The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if it exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.
