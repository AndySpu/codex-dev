# codex-dev

## Environment

- `sandbox_mode`: workspace-write
- `network_access`: restricted
- `writable_root`: /home/aggro/dev/aggro-dev/codex-dev
- `shell`: bash
- `maven`: Apache Maven 3.6.3 (`/opt/apache-maven-3.6.3`)
- `java`: Oracle JDK 22.0.2 (`/home/aggro/dev/tools/jdk-22.0.2`)

### Git

- Из-за ограниченного сетевого доступа попытки `git push` из песочницы завершаются ошибкой `Could not resolve host: github.com`.
- Для отправки коммитов на origin используйте свою машину или среду с доступом к GitHub.
- Если нужно доставить изменения из песочницы, выполните `git format-patch` или `git diff` и перенесите патч в окружение с сетью, затем примените его и выполните `git push` оттуда.
  - Пример: `git format-patch -1 HEAD` сохранит последний коммит в файл, который можно перенести и применить в другой среде через `git am`. Для незакоммиченных правок используйте `git diff > changes.patch` и применяйте через `git apply`.
