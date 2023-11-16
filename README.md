# Tun2SocksKit

[![Загрузки][0]][1]

[0]: https://img.shields.io/github/downloads/arror/Tun2SocksKit/total.svg
[1]: https://github.com/arror/Tun2SocksKit/releases/latest

⚠️⚠️⚠️ Не гарантируется работоспособность каждой версии, пожалуйста, [сделайте Fork](https://github.com/daemooon/Tun2SocksKit/fork) для публикации ⚠️⚠️⚠️

### Важные изменения

> `2.4.0` Поддержка maccatalyst (arm64, x86_64) от [@hossinasaadi](https://github.com/hossinasaadi)

> `2.2.1` Поддержка macOS (arm64, x86_64)

> ~~`2.2.0` Поддержка macOS (arm64, x86_64)~~

> `2.1.16` Поддержка iPhone симулятора, реализация через [hev-socks5-tunnel-iphonesimulator](https://github.com/daemooon/hev-socks5-tunnel-iphonesimulator)

> ~~`2.1.10` Поддержка симулятора arm64~~

> `2.0.1` Использование [hev-socks5-tunnel](https://github.com/heiher/hev-socks5-tunnel) вместо [leaf](https://github.com/eycorsican/leaf)

### Использование
```swift
import Tun2SocksKit

Socks5Tunnel.run(withFileDescriptor: 4, configFilePath: localConfigFileURL.path(percentEncoded: false))
```

### Конфигурационный файл (см. подробнее в hev-socks5-tunnel)[hev-socks5-tunnel](https://github.com/heiher/hev-socks5-tunnel)）
```yml
tunnel:
  mtu: 9000

socks5:
  port: 7890
  address: ::1
  udp: 'udp'

misc:
  task-stack-size: 20480
  connect-timeout: 5000
  read-write-timeout: 60000
  log-file: stderr
  log-level: debug
  limit-nofile: 65535
```






