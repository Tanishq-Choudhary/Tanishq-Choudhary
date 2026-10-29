Final-year Computer Science student at Manipal University Jaipur, graduating July 2027. I build backend systems, mostly in Java and Spring, and then try to make them fall over on purpose. Longer writeups, with the numbers and how they were measured, are on [tanishqchoudhary.vercel.app](https://tanishqchoudhary.vercel.app).

### Projects

- [**Rook**](https://github.com/Tanishq-Choudhary/rook): patches code broken by SDK changes and proves each patch in a sandbox. 56 of 56 on a held-out set, no escaped regressions.
- [**Mercury**](https://github.com/Tanishq-Choudhary/mercury): trade settlement pipeline with a transactional outbox and idempotent consumers. A chaos endpoint stops a live Kafka consumer mid-load; 39,716 trades at 661 a second, every one settled.
- [**Sift**](https://github.com/Tanishq-Choudhary/sift): network anomaly detector that parses packets byte by byte. Two lock-contention fixes found with thread dumps took it from 19,000 to 343,000 packets a second with zero dropped.
- [**Pulse**](https://github.com/Tanishq-Choudhary/pulse): on-call assistant with feedback-based re-ranking. EXPLAIN ANALYZE showed Postgres ignoring the vector index; a two-stage query brought the median from 261 ms to 13.9 ms.

### Open source

Fixes merged into other people's projects:

| Project | Fix |
|---|---|
| Spring Framework | `RetryPolicy` built from a builder changed which exceptions it retried when the builder was reused after `build()` ([#37596](https://github.com/spring-projects/spring-framework/pull/37596)) |
| Guava | Entries of a filtered multimap accepted `setValue` with a value the filter rejects ([#8781](https://github.com/google/guava/pull/8781), landed as [37535d73f](https://github.com/google/guava/commit/37535d73f)) |
| Spring Integration | The PostgreSQL subscribable channel retried a failed message by default; backported to 7.1.x and 7.0.x ([#11566](https://github.com/spring-projects/spring-integration/pull/11566)) |
| Spring AMQP | Address resolver and connection back-off never reached the publisher connection factory; backported to 4.1.x and 4.0.x ([#3740](https://github.com/spring-projects/spring-amqp/pull/3740)) |
| node-redis | Binary stream names corrupted by RESP3 `XREAD` ([#3540](https://github.com/redis/node-redis/pull/3540)), `ARINFO FULL` averages returned as strings on RESP2 ([#3550](https://github.com/redis/node-redis/pull/3550)), Buffer attributes mangled by `vSetAttr` ([#3552](https://github.com/redis/node-redis/pull/3552)) |
| H2 Database | Window functions in `WHERE` or `HAVING` were accepted and returned no rows ([#4487](https://github.com/h2database/h2database/pull/4487)) |
| Prometheus client_java | Metric-specific properties lost the case of the metric name ([#2588](https://github.com/prometheus/client_java/pull/2588)) |

### Elsewhere

[Resume and writeups](https://tanishqchoudhary.vercel.app) | tanishqchoudhary007@gmail.com
