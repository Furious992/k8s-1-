# Домашнее задание: Pod и Service в Kubernetes (MicroK8s)

## Задание 1. Pod hello-world

Манифест Pod: [manifests/hello-world-pod.yaml](manifests/hello-world-pod.yaml)

### Проверка Pod
Вывод команды:

`microk8s kubectl get pods -o wide`

![hello-world get pods](./screenshots/01-hello-world-get-pods.png)

### Подключение через port-forward
Команда:

`microk8s kubectl port-forward pod/hello-world 8080:8080`

Результат подключения (curl или браузер):

![hello-world curl](./screenshots/02-hello-world-curl.png)

---

## Задание 2. Pod netology-web + Service netology-svc

Манифест Pod: [manifests/netology-web-pod.yaml](manifests/netology-web-pod.yaml)  
Манифест Service: [manifests/netology-svc.yaml](manifests/netology-svc.yaml)

### Проверка Pod
Вывод команды:

`microk8s kubectl get pods -o wide`

![netology-web get pods](./screenshots/03-netology-web-get-pods.png)

### Проверка Service
Вывод команды:

`microk8s kubectl get svc -o wide`

![netology-svc get svc](./screenshots/04-netology-svc-get-svc.png)

### Подключение к Service через port-forward
Команда:

`microk8s kubectl port-forward svc/netology-svc 8081:80`

Результат подключения:

![netology-svc curl](./screenshots/05-netology-svc-curl.png)
