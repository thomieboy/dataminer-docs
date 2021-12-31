## Configuring DataMiner Indexing

To configure the DataMiner Indexing settings, go to *System Center* > *Search & Indexing*.

The following options are available:

- *Enable indexing on alarms: *Enables indexing of alarms. If this option is not enabled, the enhanced search options in the Alarm Console are not available.

- *Migrate booking data to Indexing Engine*: Starts a wizard that allows you to migrate booking data from the Cassandra database to the Indexing database. Only displayed in case booking data have not been migrated yet.

    Please note the following regarding the migration of booking data:

    - Property names in the Indexing Engine must not start with an underscore (“\_”) or contain any of the following characters: . # \* , " '<br>As such, the wizard will ask you to rename certain booking properties before starting the migration. To ensure the correct functionality of the Service & Resource Management module, some properties will be renamed automatically. For example, the *Visual.Background* and *Visual.Foreground* properties will automatically be renamed as *VisualBackground* and *VisualForeground*.

    - After migrating the booking data to the Indexing database, make sure to check your Automation scripts and Visio files and adjust the booking property names where necessary.

    - After the migration is complete, you can use the *Retrieve report* button in the wizard to get a summary report of the migration.

    - An Indexing database takes about twice as much disk space to store booking data compared to a Cassandra database.

> [!NOTE]
> -  The Indexing Engine configuration is saved in the file *Indexing.xml* in the folder *C:\\Skyline DataMiner*.
> -  To include booking data from the Indexing database in a custom backup, select *Include SRM in backup* in the content tab of the *Backup* page. See [Configuring the DataMiner backups](../DataminerAgents/Backing_up_a_DataMiner_Agent_in_DataMiner_Cube.md#configuring-the-dataminer-backups).

> [!TIP]
> See also:
> [Indexing database settings](../../part_7/SkylineDataminerFolder/DB_xml.md#indexing-database-settings)