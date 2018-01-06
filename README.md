Repository of package metadata
==============================

Some software packages don't provide their metadata in a machine readable
format.
To allow processing them in an automated fashion this repository makes these
information available, e.g. for the command line tool `colcon`.

How to use the Information
--------------------------

To register this repository with `colcon` (using the identifier "default")
invoke the following command:

```
colcon metadata add default https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml
```

Afterwards as well as on a regular base fetch the latest content from the
repository:

```
colcon metadata update default
```

How to contribute additional information
----------------------------------------

Initially fork this repository.
For each contribution perform the following steps:

* Create or modify one or multiple files ending with `.meta`.
* Add any new files in alphabetical order to the `index.yaml` file.
* Run the `lint.py` script to ensure that the changes follow the recommended
  yaml style.
* Create a pull request with the changes.
