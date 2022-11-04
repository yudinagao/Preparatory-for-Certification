# Design for backup and recovery

## Requirements

- Identify business Needs
- Builiding Resiliency plan
    - What are your workloads and their usage?
    - What are the usage patterns for your workloads?
    - What are the availability metrics?
    - What are the recovery metrics?
    - What are the workload availability targets?
    - What are your SLAs?

## Azure Backup

- On-premises
- Azure VM
- Azuure Files Share
- Microsoft SQL Server in Azure VMs
- SAP HANA databases in Azure Vms
- Microsfot Cloud

### Backup Vault x Recovery Services Vault

- Think about how to organize the vaults
- Use Azure policy
- Protect using Azure Role Based Access Control (RBAC)
- Design for Redundancy

## Azure Blob Backup and Recovery

- local
- Container soft Delete
- Blob soft Delete
- Blob Versioning
- Point in time Recovery
- Use Resource Locks

## Azure files backup and recovery

- Share snapshots capture the share state at that point in time.
- Snapshots can be created Manually - root level
- Snapshot can be automated using Azure backup and backup Policy
- can be read, copied not modified

### Considerations

- Use instant restore
- Implement alerting and reporting
- Self Service restore
- Organize files for Backup or on-demand
- Snapshot before code deployment

## Azure VM backup and recovery

- Identify best backup schedule 
- Backup Frequency
- Backup Policies
- Monitor and review your plan
- Practice restoring from backup
- Consider Throttling
- Consider Cross Region Restore

## Azure SQL backup and Recovery

- Full Backups
- Differential backups
- Transactional backups

- restore to a point in time
- restore a deleted database
- restore a database to another geographic region
- restore a database from  a specific long-term backup

## Azure Site Recovery

- automate disaster recovery