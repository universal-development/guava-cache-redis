# guava-cache-redis

Fork of https://github.com/levyfan/guava-cache-redis with updated dependencies and better error handling.

## Usage

Usage in gradle:

`build.gradle`
```
    repositories {
        maven {
            url "https://mvn.universal-development.com/public" 
        }
    }

    dependencies {
        implementation 'com.unidev.cache:guava-cache-redis:0.1.0'
    }
```

Java usage:
```
        GenericObjectPoolConfig<Jedis> jedisConfig = new GenericObjectPoolConfig<>();

        JedisPool jedisPool = new JedisPool(jedisConfig, address, port);

        redisCache = new RedisCache<>(
                jedisPool,
                new JdkSerializer(),
                new JdkSerializer(),
                "test-prefix".getBytes(StandardCharsets.UTF_8),
                666
        );
```
