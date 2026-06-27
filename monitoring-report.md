# Portfolio-05: Monitoring

## Что сделано
- Установлен Prometheus + Grafana через MicroK8s observability
- Настроен сбор метрик с nginx-пода
- Проверена доступность метрик через Prometheus API

## Доступные метрики
- up — статус всех сервисов (1 = работает)
- nginx_http_requests_total — количество запросов к nginx
- container_cpu_usage — нагрузка на процессор
- container_memory_usage — потребление памяти

## Команды
- Включение мониторинга: `sudo microk8s enable observability`
- Проверка подов: `sudo microk8s kubectl get pods -n observability`
- Запрос метрик: `curl -s http://localhost:9090/api/v1/query?query=up`
