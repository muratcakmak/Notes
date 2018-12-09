# Redis

## What is Redis?

- In-memory data structure store
- NoSQL key/value
- Supports Multiple Data Structures
- Built In Replication 🕵️‍

## Datatypes

- Strings
- Lists
- Sets
- Sorted Sets
- Hashes
- Bitmaps
- Hyperlogs
- Geospatial Indexes

## Advantages

- Very flexibles
- Fast
- Rich Datatyoe Support
- Caching and Disc Performant

## Languages

- Most of the high level languages

```
Trusted clients can access redis
```

Install `redis-cli`

Fundamental Redis Commands

### GET

`GET server:name`

### SET

`SET server:name some server`

### MSET

`MSET key1 "Hello" key2 "World"`

### APPEND

`APPEND key1 " World"`

### RENAME

`RENAME key1 greeting`

### SETEX

`SETEX greeting 30 "Hello world"`

### PERSIST

`PERSIST greeting`

### EXPIRE

`EXPIRE greeting 50`

### TTL

`TTL greeting`

### EXISTS

### DEL

### FLUSHALL

Remove Everything

### INCR

### DECR

### LPUSH

`LPUSH people "Oguzhan"`

`LPUSH people "Dan"`

`LPUSH people "J"`

### LRANGE

`LRANGE people 0 -1`

`LRANGE people 1 2`

### LLEN

`LLEN people`

### LPOP

### RPOP

### LINSERT

### RPUSH
