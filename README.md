# PHPStorm error

## Steps to reproduce

1. Go to Settings / PHP
2. Click the `...` next to CLI Interpreter
3. Click the + in the top left to add a new one and select "From Docker, Vagrant..."
4. Select the docker-compose option

The error appears as in `error-screenshot.png`.

## Fix

Removing lines 5 and 6 (the `extra_hosts`) of the `docker-compose.yml` fixes the
problem.

I was also able to get it working by removing the lines, following the
steps above without adding the new CLI Interpreter, then adding the lines back
in before following the steps above again. The list of services seemed to be
cached. Changing the `docker-compose.yml` file again made the problem recur.
