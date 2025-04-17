# Last Git Tag
## Description
This tool check all existing (local) git tags in a repository and return the last tag, and possible next tags.

## License
GNU General Public License (GPL) v3

## Installation
### Requirements
- **Python version**: >= 3.12.0<br>
- **Git**

To install this tool just copy the file into /usr/bin and set execution permissions (chmod 755).

## Usage examples
Without given prefix:
```shell
user@machine:/path/to/repository$ lastgittag
Looking for latest tag without prefix ... 
Total tags found: 218
Latest tag is: 1.361.20
Next possible MAJOR version: 2.0.0
Next possible MINOR version: 1.362.0
Next possible PATCH version: 1.361.21
```
With given prefix:
```shell
user@machine:/path/to/repository$ lastgittag -p release-
Looking for latest tag with "release-" prefix ... 
Total tags found: 4812
Latest tag is: release-1.367.126
Next possible MAJOR version: release-2.0.0
Next possible MINOR version: release-1.368.0
Next possible PATCH version: release-1.367.127
```
Show help:
```shell
user@machine:/path/to/repository$ lastgittag -h
USAGE: lastgittag --prefix=<tag-prefix>
-h				Shows this help
-p	--prefix=<tag-prefix>	Git tag prefix
-V	--version		Print the version of the lastgittag tool
-v	--verbose		Verbose output
```