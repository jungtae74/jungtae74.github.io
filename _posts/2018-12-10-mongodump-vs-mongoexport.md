---
layout: post
title: mongodump 와 mongoexport 비교
category: [mongodb, 데이터베이스]
tags: [mongodb, mongodump, mongoexport]
---

비슷한듯 다른 MongoDB Tools 비교

|               | [mongodump] | [mongoexport] |
|---------------|:---------:|:-----------:|
| 압축 지원   | [O][gzip] | X |
| 컬렉션 정보 | O | X |
| 인덱스      | O | X |
| 데이터 형식 | BSON (바이너리) | JSON, CSV (텍스트) |
|---
| Project | X | [O][project] |
| Skip    | X | [O][skip]    |
| Limit   | X | [O][limit]   |
| Sort    | X | [O][sort]    |

[mongodump]: https://docs.mongodb.com/manual/reference/program/mongodump/
[mongoexport]: https://docs.mongodb.com/manual/reference/program/mongoexport/
[gzip]: https://docs.mongodb.com/manual/reference/program/mongodump/#cmdoption--gzip
[project]: https://docs.mongodb.com/manual/reference/program/mongoexport/#cmdoption--fields
[skip]: https://docs.mongodb.com/manual/reference/program/mongoexport/#cmdoption--skip
[limit]: https://docs.mongodb.com/manual/reference/program/mongoexport/#cmdoption--limit
[sort]: https://docs.mongodb.com/manual/reference/program/mongoexport/#cmdoption--sort

