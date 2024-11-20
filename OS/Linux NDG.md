==Arguments==

```bash
command [options…] [arguments…]
```

==Printing Working Directory==

```bash
pwd [OPTIONS]
```
![[Screenshot 2024-11-06 104621.png]]

==Listing Files==
![[Screenshot 2024-11-06 110822.png]]

==dd commands==
Команда `dd` в Linux используется для низкоуровневого копирования и преобразования данных. Она может копировать данные из одного файла или устройства в другое, а также позволяет создавать образы дисков, делать резервные копии, восстанавливать данные и перезаписывать данные на устройствах.

## Iptables

-  **Таблицы (`tables`)**: `iptables` поддерживает несколько таблиц, каждая из которых имеет своё назначение:
    
    - **filter** (по умолчанию) — для фильтрации пакетов.
    - **nat** — для сетевого адреса перевода (Network Address Translation).
    - **mangle** — для модификации заголовков пакетов.
    - **raw** — для особой обработки пакетов (например, чтобы избежать отслеживания состояния).
- **Цепочки (`chains`)**: Таблицы содержат цепочки, которые представляют собой последовательности правил:
    
    - **INPUT** — для входящих пакетов, адресованных локальной системе.
    - **OUTPUT** — для исходящих пакетов, отправляемых с локальной системы.
    - **FORWARD** — для пакетов, проходящих через систему (например, при настройке роутера).
    - **PREROUTING** — для обработки пакетов до маршрутизации.
    - **POSTROUTING** — для обработки пакетов после маршрутизации.
- **Правила (`rules`)**: Это отдельные инструкции, которые говорят, что делать с пакетом (разрешить, отклонить и т. д.). Правила включают условия (например, IP-адреса, порты, протоколы) и действия (`target`).

#### Основные команды `iptables`

- `-A` (Append): Добавить правило в конец цепочки.
- `-I` (Insert): Вставить правило в цепочку на указанную позицию.
- `-D` (Delete): Удалить правило из цепочки.
- `-L` (List): Показать все правила в цепочке.
- `-F` (Flush): Удалить все правила в цепочке.
- `-P` (Policy): Установить политику по умолчанию для цепочки (например, ACCEPT или DROP).