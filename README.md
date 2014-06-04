# libriskiq

*Python client API for RiskIQ services*

**libriskiq** provides a Python client library implementation into RiskIQ API
services. The library currently provides support for the following services:

- Passive DNS queries
- Blacklist URL search
- Blacklist Incident URL search
- ZList download
- Crawler *Landing Page* submission

## Command-line scripts

The following command line scripts are installed with the library:

- **`riq-config`**: utility to set API configuration options for the library (API token and private key).
- **`riq-pdns`**: client to issue queries to the RiskIQ Passive DNS database service.

## Installation

    $ python setup.py install

The package depends on the [Requests](http://docs.python-requests.org/) library.
If Requests is not installed, it will be installed as a result of the above command.

## Setup

First-time setup requires configuring an API token and private key for authentication.

    $ riq-config -t <API_TOKEN> -k <API_PRIVATE_KEY>

At any time, the current API configuration parameters can be queried using the same utility:

    $ riq-config -p

Configuration parameters are stored in `$HOME/.config/riskiq/api_config.json`.

