Blackfire
=========

Install and configure blackfire APM for php

Requirements
------------

Works great with php-fpm

Role Variables
--------------

```
# Blackfire install configuration
blackfire_key_url: https://packagecloud.io/gpg.key
blackfire_package_url: http://packages.blackfire.io/debian
blackfire_directory: /etc/blackfire

# Blackfire agent configuration
blackfire_cert:                                          # Sets the PEM encoded certicates
blackfire_collector: https://blackfire.io                # Sets the URL of Blackfire's data collector
blackfire_http_proxy:                                    # Sets the http proxy to use
blackfire_https_proxy:                                   # Sets the https proxy to use
blackfire_log_file: stderr                               # Sets the path of the log file. Use stderr to log to stderr
blackfire_log_level: 1                                   # log verbosity level (4: debug, 3: info, 2: warning, 1: error)
blackfire_server_id: "REPLACE_IT_WITH_YOUR_KEY"          # Sets the server id used to authenticate with Blackfire API
blackfire_server_token: "REPLACE_IT_WITH_YOUR_KEY"       # Sets the server token used to authenticate with Blackfire API. It is unsafe to set this from the command line
blackfire_socket: "unix:///var/run/blackfire/agent.sock" # Sets the socket the agent should read traces from. Possible value can be a unix socket or a TCP address
blackfire_spec:                                          # Sets the path to the json specifications file
```

Example Playbook
----------------

```
    - hosts: servers
      roles:
         - { role: jebovic.blackfire }
```

License
-------

MIT

Author Information
------------------

Jérémy Baumgarth https://github.com/jebovic