To demonstrate the bug:

1. Run the root compose file:

```
$ docker-compose up
```

2. Run the nested compose file:
 ```
 $ docker-compose -f docker-compose.yml -f services/servicea/docker-compose.yml up --force-recreate
```

Will generate an error with "stacking" relative paths to the env file


`ERROR: Couldn't find env file: /home/nick/tmp/composebug/services/servicea/services/servicea/env_file`
