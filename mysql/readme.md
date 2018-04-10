## Solve ERROR 2006 (HY000) at line xxx: MySQL server has gone away

This should work in most cases:

#### locate `my.cnf` file
```
locate my.cnf
```

#### update line max_allowed_packet

set `max_allowed_packet=xxM` to `max_allowed_packet=64M`
