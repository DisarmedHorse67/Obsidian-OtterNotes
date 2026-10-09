Key Words:
Automated deployments, Zero-Downtime,  EC2, ECS, Lambda, Rollback.

What is it:
This service is a deployment automating tool, it can deploy code on compute environments. It i mainly used for update apps minimizing downtime and managing rollbacks if any error ocurres. It has 3 main deploy strategies:
* In-Place: Update existing instances one by one or by batch.
* Blue/Green: It creates a new identical environment (green), deploys the new version and deviates the traffic gradually breaking the old environment (blue).
* Canary/Linear: Useful for lambda and ECS, sent 10% of the traffic for a few minutes before sending 100% of the traffic.

Use Cases:
Update and deploy EC2, ECS and Lambda codes.