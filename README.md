# logparse

Logparse is a shell script that parses Caddy JSON log files and outputs them as formatted text. It supports the Common Log Format and Combined Log Format, usually used by traditional HTTP servers like Apache, however it is easy to customise the output using the --selector option or by using a config file. Logparse uses the powerful jq tool to process the JSON logs.