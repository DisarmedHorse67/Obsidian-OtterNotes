Key Words:
Block storage, unmanaged, One Zone.

What is it:
This service storage data in blocks, so when you need to modify something, it just modifies the exact block of data that you need instead of the hole file, with this service you need to manage the formatting, file system and snapshots. This can only connects to a single EC2 instance, but an EC2 instance can have multiple EBS services.

Use Cases:
Data Bases (PostgreSQL, MySQL, etc), enterprise apps and boot volumes that requires high I/OPS and low latency

Extras:
* S3 File Gateway: Exposes S3 objects as NFS/SMB file shares to on-prem apps.
* Volume Gateway: Provides block storage volumes (iSCSI) backed by cloud snapshots.
* Tape Gateway: Replaces physical magnetic tape backups with virtual tapes in S3/Glacier.