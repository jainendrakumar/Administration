# Administration

Contains the Scripts for followig:

<BOLD>DiskUsageStats</BOLD>

<P>Share the MS SQL Server disk usage summary as follows.</P>
Category	Information	logical_volume_name	volume_mount_point	file_system_type	TotalSpace_MB	FreeSpace_MB	is_compressed
Information	Disk_Space	LOG	F:\	NTFS	204796	85931	0
Information	Disk_Space	DATA	D:\	NTFS	204796	121701	0

ShrinkAllDatabase

Shrink All Database Files in a MS SQL Database Server

This script Truncate All Transaction Logs and Shrink All Database Files for all databases within a database server.

Note: This may take many hours on a MS SQL server hosting many databases. So advice to run during off peak hours once in month.

ReIndexAll
Re index all tables @databases in a MS SQL Database Server

This script allows you to rebuild indexes for all databases and all tables within a database server.

The script uses two cursors one for the databases and another for the tables within the database.  
In addition, it uses the INFORMATION_SCHEMA.TABLES view to list all of the tables within a database.

We use the Transact-SQL programming language utility DBCC DBREINDEX to do re-index and pass parameter table and fillfactor to it.

Note: This may take many hours on a MS SQL server hosting many databases. So advice to run during off peak hours once in month.
