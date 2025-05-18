# Sqlite Filesystem
This crate is an extension for sqlite that adds some file operations to sqlite. It is implemented using sqlite-loadable.

## Operators
### Exists
```
SELECT exists('path/to/file');
```
Checks the given path and returns true, if the file or directory exists.

### New
```
SELECT fs_new('path/to/file/file_name.txt');
```
Create a new file using the given file name. Returns true, if the file could be created and exists after the operation is done.

### Delete
```
SELECT fs_delete('path/to/file/file_name.txt');
```
Delete a file from disk. Returns true, if the file was actually delete and false if the file did not exist. If an error occured the query will fail.

### Make Directory
```
SELECT fs_mk_dir('path/to/directory');
```
Create a new directory. Returns true, if the directory could be created and exists after this operation is done.

### Remove Directory
```
SELECT fs_rm_dir('path/to/directory');
```
Remove an empty directory. Returns truem, if the directory could be removed successfully.

## Tables
### List

