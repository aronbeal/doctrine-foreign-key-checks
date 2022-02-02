# doctrine-foreign-key-checks
Custom command for doctrine foreign key check toggling.

Added in response to https://github.com/doctrine/migrations/issues/43.  
Intended for use in conjunction with `doctrine:fixtures:load`, e.g.:
```bash
#!/bin/bash
doctrine:schema:toggle-foreign-key-checks 0 \
  && doctrine:fixtures:load --purge-with-truncate \
  && doctrine:schema:toggle-foreign-key-checks 1;
```

## Usage:

- Include the command in the appropriate directory in your Symfony repository.
- Invoke as a console command, e.g. ` doctrine:schema:toggle-foreign-key-checks 1` or `doctrine:schema:toggle-foreign-key-checks 0`
