# People

A server to perform CRUD operations on `people` tables.

## Table details

This table is meant to store credentials for organizations and their members.

It can be roughly defined by `O(M * N)`

Where `M` is the number of organizations at tmk3 (including tmk3) and `N` is the number of members.

## Schema

The `people` will use a snowflake-like unique id system.

The default `org_id` is `tmk3` itself.

```
id NUMERIC
org_id NUMERIC
username VARCHAR(320)
password VARCHAR(256)
password_params VARCHAR(256)
is_deleted BOOLEAN
```

Ancillary tables like `contact_info` and `payments` can point to `people:id` as a reference.
