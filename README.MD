AWS Cloud Cost Optimization - Identifying Stale Resources

Here in this project: Identifying Stale EBS Snapshots

We'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.
And this lambda function can schedule to run for example: every week to identify and delete stale resources week by week.

Description:

The Lambda function(using python) fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.

Reference: AWS SDK for Python (Boto3)
https://boto3.amazonaws.com/v1/documentation/api/latest/index.html