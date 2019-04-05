# Dataset Reader for XML Files

As a base class I'll use the library's already-implemented `TaggingDatasetReader` class.

The `TaggingDatasetReader` class- a base class for reading datasets for tagging tasks- has the following methods that we're interested in:

- \_read\_dataset
- text\_to\_instance

# The Tedious Bit: Parsing XML

