# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.2.1] - 2020-07-15

### Added

- GetAllKeys() feature to get all the Keys from Cache object
- GetAllValues() feature to get all the Values from Cache object
- HasKey(key, out result) which checks if key is in the Cache with valid expariation date

### Changed
- Fixed serialization bug which made string keys from getAllKeys not valid for cache.

## [0.2.2] - 2021-02-10

### Added
- Redis cache implemented trough, constructor customizable
- GetAllKeys() feature to get all the Keys from Cache object, works with Redis too
- GetAllValues() feature to get all the Values from Cache object, does not work with Redis cache
- HasKey(key, out result) which checks if key is in the Cache with valid expariation date, works with Redis too without out parameter

### Changed
- Fixed serialization bug which made string keys from getAllKeys not valid for cache.

### Known Issues
- GetAllKeys() works with Redis only if the port number is set in the configuration, gets all the keys from Redis cache not only which is meant for that region
- HasKey() finds all the keys located in the Cache not just for that region

## [0.2.5] - 2021-05-26

### Added
- Memory and Redis cache now accept sliding expiration during Insert
- Sliding expiration's default is half of the absolute expiration
- Remove method to delete cache key entry
- RemoveAsync to delete cache key entry async

### Changed
- GetAllKeys() now returns keys without type key for Redis Cache

## [0.2.6] - 2021-09-30

### Added
- HasKeyAsync() for universal and redis cache
- HasKey() without item return for universal and redis cache

### Changed
- Asynchronous expiration update after getting an item from redis cache

## [0.2.7] - 2021-11-22

### Breaking Changed
- ACIM.Sales-Namespaces renamed to Anexia.Caching-Namespaces

## [0.2.8] - 2022-02-14

### Fix
- Fixed issue, where getting all keys from a redis cache database doesn't work when having connection options defined in the redis' connection string
 