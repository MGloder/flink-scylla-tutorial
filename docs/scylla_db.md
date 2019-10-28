# SSTables

##[Reference Link](http://distributeddatastore.blogspot.com/2013/08/cassandra-sstable-storage-format.html)

### SSTable -> Sorted Strings Table

The data in a SSTable is organized in six types of component files.  The format of a SSTable component file is
<keyspace>-<column family>-[tmp marker]-<version>-<generation>-<component>.db

<keyspace> and <column family> fields represent the Keyspace and column family of the SSTable, <version> is an alphabetic string which represents SSTable storage format version, <generation> is an index number which is incremented every time a new SSTable is created for a column family and <component> represents the type of information stored in the file. The optional "tmp" marker in the file name indicates that the file is still being created. The six SSTable components are Data, Index, Filter, Summary, CompressionInfo and Statistics.

