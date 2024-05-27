# logparse

Logparse is a shell script that parses Caddy JSON log files and outputs them as formatted text. It supports the Common Log Format and Combined Log Format, usually used by traditional HTTP servers like Apache, however it is easy to customise the output using the --selector option.

The config file allows for changing default output format, add additional selectors and adapt logparse to other JSON sources. Logparse uses the powerful `jq` tool to process the JSON files.

## Requirements

* Bash 5.1: Logparse is using associative arrays which is not available in plain POSIX shell scripts.
* jq 1.7: Tested with jq 1.7.1.

## Usage

```text
Usage: /usr/bin/logparse [-c | -C | -s "selectors"] [-F <config_file>] filename
Options:
  -c, --common       Apache Common Log Format (default)
  -C, --combined     Apache Combined Log Format
  -s, --selector     Use a space separated list of selectors
  -F, --config-file  Use a configuration file
  -h, --help         Show this help message and exit
```

## Examples

Example usage and descriptions is available on the wiki https://wiki.tnonline.net/w/Linux/logparse