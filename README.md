Usage:

Help summary:

    cping --help

Ping google.com with default settings:

    cping google.com

Ping google.com with notifications turned off, disabled system bell
beeps, stdout and stderr piped to tee and logged to cping.log

    cping -N -s google.com | tee -a cping.log
