# Redis DeNA

Redis DeNA has following additional features against original Redis:
- 2.6.17-dena: 2.6.17 (2fc65c844f62897ddaf8f5e0f8352f3af02e91f7)
- 2.6.9-dena: 2.6.9 (c17a7f6fbc82dc6ab34a788f65adc16e84b5777c)

- ZRANK, ZREVRANK ability to return "unique" rank
    - ZRANK/ZREVRANK key member unique
    - issue: [#943](https://github.com/antirez/redis/issues/943)
- Control whether a redis slave will automatically try to reconnect/resync with the master if connection is lost (8171a22d2f2c0f39c0db784b4c6a826849f89ba9)
    - ```repl-auth-resync yes|no``` (redis.conf)
    - Default is 'yes' (auto reconnect and resync with the master)
    - issue: [#387](https://github.com/antirez/redis/pull/387)
- Call bind(2) before connect(2) if exists bind ADDR in redis.conf (003c1634b0a78f3720d6e7a9ca9723a25d95ce9b)
    - issue: [#1155](https://github.com/antirez/redis/pull/1155)

