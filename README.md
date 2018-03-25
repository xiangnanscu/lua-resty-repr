# lua-resty-repr
Convert a lua table whose key or value could be a function, userdata, thread or circular reference to a human readable and js syntax compatible string.

# Requirements
Nothing.

# Synopsis
```lua
local repr = require "resty.repr"

local t = {} -- your fancy table
local res = repr(t) -- use the default settings
res = repr:new{indent=4, max_depth=3}(t)  -- custom

```
sample out put of an instance of [lua-resty-model](https://github.com/xiangnanscu/lua-resty-model)
```js
{
  /*41570c18*/
  __index           : {/*41570c18*/},
  _referenced_models: [
    /*404c6170*/
  ],
  admin             : {
    /*41570de0*/
    filter_field_names: [
      /*41570e08*/
      "permission",
    ],
    list_display_names: [
      /*41570f80*/
      "username",
      "permission",
      "phone",
      "utime",
    ],
    search_names      : [
      /*41570c40*/
      "username",
      "phone",
    ],
  },
  age               : "function: 0x404c4f28",
  csny              : "function: 0x404c4f08",
  fields            : [
    /*4157d388*/
    {
      /*404c4fd0*/
      client_to_lua : "function: 0x41570d78",
      db_to_lua     : "function: 0x40d7ae58",
      db_type       : "integer",
      error_messages: [
        /*404c4ff8*/
      ],
      label         : "id",
      lua_to_client : "function: 0x40d698d8",
      lua_to_db     : "function: 0x40d698d8",
      name          : "id",
      null          : true,
      primary_key   : true,
      validators    : {
        /*404c57f8*/
        client_to_lua: [
          /*404c5890*/
          "function: 0x40d845b8",
          "function: 0x404d5790",
        ],
        db_to_lua    : [
          /*41a34220*/
          "function: 0x40d7ae58",
        ],
        lua_to_client: [
          /*404c60d0*/
        ],
        lua_to_db    : [
          /*404c5048*/
        ],
      },
    },
    {
      /*4157d3f0*/
      1             : "id",
      client_to_lua : "function: 0x4149b9e0",
      db_to_lua     : "function: 0x40d7ae58",
      db_type       : "integer",
      disabled      : true,
      error_messages: [
        /*4157c8c8*/
      ],
      label         : "id",
      lua_to_client : "function: 0x40d698d8",
      lua_to_db     : "function: 0x40d698d8",
      name          : "id",
      null          : true,
      primary_key   : true,
      validators    : {
        /*4157c828*/
        client_to_lua: [
          /*4157c8a0*/
          "function: 0x40d845b8",
          "function: 0x404d5790",
        ],
        db_to_lua    : [
          /*414a35e8*/
          "function: 0x40d7ae58",
        ],
        lua_to_client: [
          /*4157c2f8*/
        ],
        lua_to_db    : [
          /*4157c280*/
        ],
      },
    },
    {
      /*414a3700*/
      1             : "username",
      2             : "name",
      client_to_lua : "function: 0x41e17fa0",
      db_to_lua     : "function: 0x40d7ae58",
      db_type       : "varchar",
      error_messages: [
        /*4157c320*/
      ],
      hint          : "please enter your name",
      index         : true,
      label         : "name",
      lua_to_client : "function: 0x40d698d8",
      lua_to_db     : "function: 0x40d698d8",
      maxlength     : 18,
      minlength     : 18,
      name          : "username",
      null          : true,
      required      : true,
      unique        : true,
      validators    : {
        /*414a4680*/
        client_to_lua: [
          /*41e17f48*/
          "function: 0x41e0ec18",
          "function: 0x41e0ebb0",
          "function: 0x41e0d170",
        ],
        db_to_lua    : [
          /*414a46f8*/
          "function: 0x40d7ae58",
        ],
        lua_to_client: [
          /*40d7e958*/
        ],
        lua_to_db    : [
          /*404c1f60*/
        ],
      },
    },
    {
      /*40d7e980*/
      1             : "phone",
      2             : "phone number",
      client_to_lua : "function: 0x405f69c0",
      db_to_lua     : "function: 0x40d7ae58",
      db_type       : "varchar",
      error_messages: [
        /*41a31d58*/
      ],
      hint          : "enter your phone number",
      index         : true,
      label         : "phone number",
      lua_to_client : "function: 0x40d698d8",
      lua_to_db     : "function: 0x40d698d8",
      maxlength     : 11,
      minlength     : 11,
      name          : "phone",
      null          : true,
      required      : true,
      unique        : true,
      validators    : {
        /*41a31c90*/
        client_to_lua: [
          /*405f6718*/
          "function: 0x405f07d8",
          "function: 0x405f0748",
          "function: 0x405a5580",
        ],
        db_to_lua    : [
          /*41a36af8*/
          "function: 0x40d7ae58",
        ],
        lua_to_client: [
          /*414a6e60*/
        ],
        lua_to_db    : [
          /*405f6a38*/
        ],
      },
    },
    {
      /*414a6e88*/
      1             : "password",
      2             : "password",
      client_to_lua : "function: 0x415d7b98",
      db_to_lua     : "function: 0x40d7ae58",
      db_type       : "varchar",
      error_messages: [
        /*405e9918*/
      ],
      hint          : "enter password (at least 6 chars)",
      label         : "password",
      lua_to_client : "function: 0x40d698d8",
      lua_to_db     : "function: 0x40d698d8",
      maxlength     : 50,
      minlength     : 6,
      name          : "password",
      null          : true,
      validators    : {
        /*414a6ec8*/
        client_to_lua: [
          /*40fd49d8*/
          "function: 0x40d845b8",
          "function: 0x40fd4970",
          "function: 0x415cedd0",
        ],
        db_to_lua    : [
          /*40d729f0*/
          "function: 0x40d7ae58",
        ],
        lua_to_client: [
          /*40d72a88*/
        ],
        lua_to_db    : [
          /*415d7c10*/
        ],
      },
    },
    {
      /*41e188e8*/
      1             : "permission",
      2             : "perm",
      choices       : [
        /*41e18928*/
        [
          /*41e18970*/
          0,
          "ordinary",
        ],
        [
          /*41e189b0*/
          64,
          "admin",
        ],
        [
          /*41e189f0*/
          128,
          "system",
        ],
      ],
      client_to_lua : "function: 0x41a37d90",
      db_to_lua     : "function: 0x40d7ae58",
      db_type       : "integer",
      error_messages: [
        /*40d8a3a8*/
      ],
      label         : "perm",
      lua_to_client : "function: 0x40d698d8",
      lua_to_db     : "function: 0x40d698d8",
      max           : 128,
      name          : "permission",
      null          : true,
      validators    : {
        /*40d8a498*/
        client_to_lua: [
          /*41a37d18*/
          "function: 0x40d845b8",
          "function: 0x404d5790",
          "function: 0x41a2c798",
          "function: 0x41a2cae0",
        ],
        db_to_lua    : [
          /*40d8a458*/
          "function: 0x40d7ae58",
        ],
        lua_to_client: [
          /*404bcf08*/
        ],
        lua_to_db    : [
          /*41a37e08*/
        ],
      },
    },
    {
      /*404bcf30*/
      1             : "utime",
      auto_now      : true,
      client_to_lua : "function: 0x40d698d8",
      db_to_lua     : "function: 0x40d7ae58",
      db_type       : "timestamp(0) with time zone",
      default       : "function: 0x415c6f50",
      error_messages: [
        /*404bd010*/
      ],
      get_default   : "function: 0x404bdbf8",
      label         : "utime",
      lua_to_client : "function: 0x40d698d8",
      lua_to_db     : "function: 0x40d698d8",
      name          : "utime",
      null          : true,
      required      : false,
      validators    : {
        /*404bdc18*/
        client_to_lua: [
          /*404bdc90*/
        ],
        db_to_lua    : [
          /*41a33be0*/
          "function: 0x40d7ae58",
        ],
        lua_to_client: [
          /*41a33c78*/
        ],
        lua_to_db    : [
          /*404bdb30*/
        ],
      },
    },
    {
      /*41a33ca0*/
      1             : "ctime",
      auto_now_add  : true,
      client_to_lua : "function: 0x40d698d8",
      db_to_lua     : "function: 0x40d7ae58",
      db_type       : "timestamp(0) with time zone",
      default       : "function: 0x415c6f50",
      error_messages: [
        /*41a34288*/
      ],
      get_default   : "function: 0x41a34378",
      label         : "ctime",
      lua_to_client : "function: 0x40d698d8",
      lua_to_db     : "function: 0x40d698d8",
      name          : "ctime",
      null          : true,
      required      : false,
      validators    : {
        /*404bcf70*/
        client_to_lua: [
          /*41a34258*/
        ],
        db_to_lua    : [
          /*404c4530*/
          "function: 0x40d7ae58",
        ],
        lua_to_client: [
          /*404c45c8*/
        ],
        lua_to_db    : [
          /*41a34300*/
        ],
      },
    },
  ],
  fields_dict       : {
    /*404c6148*/
    ctime     : {/*41a33ca0*/},
    id        : {/*4157d3f0*/},
    password  : {/*414a6e88*/},
    permission: {/*41e188e8*/},
    phone     : {/*40d7e980*/},
    username  : {/*414a3700*/},
    utime     : {/*404bcf30*/},
  },
  foreign_keys      : [
    /*404c6198*/
  ],
  name              : "guys",
  render            : "function: 0x404c61c0",
  table_name        : "user",
  sex               : "function: 0x404c6740",
}
```
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
