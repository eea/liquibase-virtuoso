
Provides a package that forms the Virtuoso-specific plugin for Liquibase.

The idea is to override some of Liquibase's default implementations for unknown databases, because they don't work out of the box with Virtuoso. These overrides include:
- creation/inserts/updates/selects on Liquibase's DATABASECHANGELOGLOCK table.
- override Liquibase's RawSQLChange to skip calling nativeSQL() method Virtuoso's JDBC connection.

Fully qualified name of this class must be fed into <databaseClass> tag of the <configuration> tag of the Liquibase Maven plugin in pom.xml.

