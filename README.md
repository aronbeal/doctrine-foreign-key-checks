# doctrine-foreign-key-checks
Custom command for doctrine foreign key check toggling.

Added in response to https://github.com/doctrine/migrations/issues/43.  
Intended for use in conjunction with `doctrine:fixtures:load`, e.g.:
```bash
#!/bin/bash
bin/console doctrine:schema:toggle-foreign-key-checks 0 \
  && bin/console doctrine:fixtures:load --purge-with-truncate \
  && bin/console  doctrine:schema:toggle-foreign-key-checks 1;
```

## Usage:

- Include the command in the appropriate directory in your Symfony repository.
- Invoke as a console command, e.g. `bin/console doctrine:schema:toggle-foreign-key-checks 1` or `bin/console doctrine:schema:toggle-foreign-key-checks 0`
