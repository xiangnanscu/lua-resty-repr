# lua-resty-validator
Convert a lua table whose key or value could be a function, userdata, thread or circular reference to a human readable and js syntax compatible string.

# Requirements
Nothing.

# Synopsis
sample out put of [resty.sql.postgresql](https://github.com/xiangnanscu/lua-resty-sql/blob/master/resty/sql/postgresql.lua)
```js
{
  /*40df5580*/
  CHAIN_METHODS   : [
    /*40ddebd0*/
    "select",
    "where",
    "group",
    "having",
    "order",
    "limit",
    "offset",
    "join",
    "create",
    "update",
    "delete",
    "distinct",
  ],
  Q               : {
    /*41bdb288*/
    __call   : "function: 0x41bdb490",
    __div    : "function: 0x41bdb468",
    __index  : {/*41bdb288*/},
    __mul    : "function: 0x41bdb338",
    __unm    : "function: 0x41bdb318",
    negated  : "",
    op       : "",
    serialize: "function: 0x41bdb4b8",
  },
  __index         : {/*40df5580*/},
  _add_to_join    : "function: 0x4041b600",
  _parse_from     : "function: 0x40df5558",
  _parse_group    : "function: 0x40df54d8",
  _parse_having   : "function: 0x4041b620",
  _parse_key_value: "function: 0x40df52f0",
  _parse_limit    : "function: 0x40df5518",
  _parse_offset   : "function: 0x40df5538",
  _parse_order    : "function: 0x40df54f8",
  _parse_params   : "function: 0x40df5440",
  _parse_select   : "function: 0x40df5468",
  _parse_where    : "function: 0x40df54b8",
  bind_model      : "function: 0x41be0b38",
  class           : "function: 0x40803ae0",
  create          : "function: 0x41be0d38",
  delete          : "function: 0x41be0d78",
  distinct        : "function: 0x41be0c68",
  escape_name     : "function: 0x4041b318",
  escape_string   : "function: 0x4041b3a0",
  escape_value    : "function: 0x4041b338",
  group           : "function: 0x41bdb2d8",
  having          : "function: 0x41be0de0",
  join            : "function: 0x41be0cf0",
  limit           : "function: 0x41be0c28",
  new             : "function: 0x41be0ab0",
  offset          : "function: 0x41be0c48",
  order           : "function: 0x41be0af8",
  select          : "function: 0x41be0ad0",
  statement       : "function: 0x41be0d10",
  to_update_sql   : "function: 0x4041b3c0",
  update          : "function: 0x41be0d58",
  where           : "function: 0x41be0d98",
}
```
