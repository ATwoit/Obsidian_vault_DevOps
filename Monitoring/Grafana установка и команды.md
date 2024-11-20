Для начало устонавливаем и обновляем пакеты:
```javascript
sudo apt-get update
sudo apt-get install -y software-properties-common
```

Добавляем репозиторий Grafana:
```javascript
sudo add-apt-repository "deb https://packages.grafana.com/oss/deb stable main"
```

Добавляем ключ репозитория Grafana:
```javascript
wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
```

Обновляем список пакетов и установливаем Grafana:
```javascript
sudo apt-get update
sudo apt-get install -y grafana
```

Запуск Grafana:
```javascript
sudo systemctl start grafana-server
sudo systemctl enable grafana-server
```