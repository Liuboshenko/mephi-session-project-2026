# MEPHI Session Project 2026 / Сессионный проект МИФИ 2026

## 🇬🇧 English

### Overview

This project demonstrates system administration skills on **Fedora 43 Server Edition**. A minimal server installation was configured for use in a local network environment, including network setup, software management, filesystem operations, access control, and web server deployment.

**Student ID:** M255604

### Completed Tasks

#### 1. Network Management (10 pts)
- Static IP configuration: `192.168.1.100/24`, gateway `192.168.1.1`, DNS `8.8.8.8`
- Hostname set to `mephi-2026.domain.local`
- Network connectivity verified (ping to gateway and external DNS)

#### 2. Software Management (10 pts)
- Installed packages via `dnf`: nginx, tcpdump, libcap-ng-utils
- Downloaded tcpdump RPM package and installed it using `rpm`

#### 3. Filesystem & Services (10 pts)
- Created partition on `/dev/sdb`, formatted as ext4 with label `MEPHI_DATA`
- Configured auto-mount via `/etc/fstab` at `/data/mephi-web`
- Enabled and started nginx web server

#### 4. Access Control (10 pts)
- **DAC:** Created user `mephi-admin` and group `mephi-devs`, set ownership and permissions (2775/setgid) on `/data/mephi-web`
- **MAC:** SELinux in Enforcing mode, applied `httpd_sys_content_t` context to web directory
- **Capabilities:** Configured `cap_net_admin,cap_net_raw=ep` on tcpdump for unprivileged execution

#### 5. Authentication & Testing (10 pts)
- Blocked root login via PAM (`pam_listfile.so`) and SSH (`PermitRootLogin no`)
- Deployed personalized web page: `Hello from Student: M255604`
- Verified nginx accessibility from localhost and network

### Project Artifacts

| File | Section | Description |
|------|---------|-------------|
| `project_history.txt` | All | Complete command history |
| `network_check.txt` | 1.2 | Ping results |
| `nginx_recent_logs.txt` | 3.2 | Nginx journal logs |
| `fstab.txt` | 3.1 | Auto-mount configuration |
| `selinux_status.txt` | 4.2 | SELinux mode |
| `file_contexts.txt` | 4.2 | SELinux file context |
| `tcpdump_capabilities.txt` | 4.2 | Capabilities configuration |
| `permissions.txt` | 4.1 | Directory permissions and ownership |
| `users_groups.txt` | 4.1 | User and group information |
| `index.html` | 5.2 | Web page |
| `curl_output.txt` | 5.2 | Web server test result |
| `mephi-nginx-screenshot.png` | 5.2 | Visual confirmation |
| `tcpdump.rpm` | 2.2 | Downloaded RPM package |

### Environment

- **OS:** Fedora Linux 43 (Server Edition)
- **Kernel:** 6.17.1-300.fc43.x86_64
- **Virtualization:** Oracle VirtualBox (Host-Only networking)

---

## 🇷🇺 Русский

### Описание

Проект демонстрирует навыки системного администрирования на **Fedora 43 Server Edition**. Минимальная серверная установка была настроена для работы в локальной сети: конфигурация сети, управление ПО, работа с файловыми системами, управление доступом и развёртывание веб-сервера.

**Номер зачётной книжки:** M255604

### Выполненные задания

#### 1. Управление сетью (10 баллов)
- Статический IP: `192.168.1.100/24`, шлюз `192.168.1.1`, DNS `8.8.8.8`
- Имя хоста: `mephi-2026.domain.local`
- Проверена сетевая связность (ping до шлюза и внешнего DNS)

#### 2. Управление программным обеспечением (10 баллов)
- Установлены пакеты через `dnf`: nginx, tcpdump, libcap-ng-utils
- Скачан RPM-пакет tcpdump и установлен через `rpm`

#### 3. Управление файловыми системами и сервисами (10 баллов)
- Создан раздел на `/dev/sdb`, отформатирован как ext4 с меткой `MEPHI_DATA`
- Настроено автомонтирование через `/etc/fstab` в `/data/mephi-web`
- Запущен и включён в автозагрузку веб-сервер nginx

#### 4. Управление доступом (10 баллов)
- **DAC:** Создан пользователь `mephi-admin` и группа `mephi-devs`, установлены права 2775 (setgid) на `/data/mephi-web`
- **MAC:** SELinux в режиме Enforcing, применён контекст `httpd_sys_content_t` к директории веб-сервера
- **Capabilities:** Настроены `cap_net_admin,cap_net_raw=ep` на tcpdump для запуска без root

#### 5. Аутентификация и тестирование (10 баллов)
- Заблокирован вход root через PAM (`pam_listfile.so`) и SSH (`PermitRootLogin no`)
- Развёрнута персонализированная веб-страница: `Hello from Student: M255604`
- Проверена доступность nginx с localhost и из сети

### Артефакты проекта

| Файл | Раздел | Описание |
|------|--------|----------|
| `project_history.txt` | Все | Полная история команд |
| `network_check.txt` | 1.2 | Результаты ping |
| `nginx_recent_logs.txt` | 3.2 | Журнал nginx |
| `fstab.txt` | 3.1 | Конфигурация автомонтирования |
| `selinux_status.txt` | 4.2 | Режим SELinux |
| `file_contexts.txt` | 4.2 | Контекст SELinux |
| `tcpdump_capabilities.txt` | 4.2 | Настройка capabilities |
| `permissions.txt` | 4.1 | Права и владелец директории |
| `users_groups.txt` | 4.1 | Информация о пользователях и группах |
| `index.html` | 5.2 | Веб-страница |
| `curl_output.txt` | 5.2 | Результат тестирования |
| `mephi-nginx-screenshot.png` | 5.2 | Визуальное подтверждение |
| `tcpdump.rpm` | 2.2 | Скачанный RPM-пакет |

### Окружение

- **ОС:** Fedora Linux 43 (Server Edition)
- **Ядро:** 6.17.1-300.fc43.x86_64
- **Виртуализация:** Oracle VirtualBox (Host-Only сеть)