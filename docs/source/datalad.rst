==================
Data management
==================

`DataLad <https://www.datalad.org/>`_ is a software tool designed to help with anything related to the version control
of of digital objects. Flexible storage options and means for retrieval and updating of data efficiently are crucial for 
data further usage. 
DataLad assists with storing and retrieving the data in a transparent and streamlined fashion, 
which aims to standardize data access and updates across hosting solutions.

Basics
---------

DataLad enables you to improve access to data from various sources in the form of a distributed network 
by registering online sources or neuroscience data platforms (such as OpenNeuro) as useful metadata for files. 
Moreover, this tool separates the actual data retrieval of the file contents from the simplified metadata based 
representation of file names, allowing you to represent datasets of any scale at a fraction of their total size on 
disk while documenting and maintaining access to them.

For full access to the contents of any dataset, use the command ``% datalad get ...`` which is specified in `Command Line Reference <http://docs.datalad.org/en/stable/generated/man/ datalad -get.html>`_ in the DataLad documentation.

In order to share data sets, it can use the standard repository hosting infrastructure (GitHub, Bitbucket and others) as access points for data installation, without actually publishing the data content in these services, which allows it to have the height of the files.


Data storage
--------------

In progress.