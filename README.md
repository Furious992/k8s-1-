# Домашнее задание: Pod и Service в Kubernetes (MicroK8s)

## Задание 1. Pod hello-world

Манифест Pod: [manifests/hello-world-pod.yaml](manifests/hello-world-pod.yaml)

### Проверка Pod
Вывод команды:

`microk8s kubectl get pods -o wide`

![hello-world get pods](https://github.com/Furious992/k8s-1-/blob/main/2.png)

### Подключение через port-forward
Команда:

`microk8s kubectl port-forward pod/hello-world 8080:8080`

Результат подключения (curl или браузер):

![hello-world curl](https://github.com/Furious992/k8s-1-/blob/main/3.png)

---

## Задание 2. Pod netology-web + Service netology-svc

Манифест Pod: [manifests/netology-web-pod.yaml](manifests/netology-web-pod.yaml)  
Манифест Service: [manifests/netology-svc.yaml](manifests/netology-svc.yaml)

### Проверка Pod
Вывод команды:

`microk8s kubectl get pods -o wide`

![netology-web get pods](https://github.com/Furious992/k8s-1-/blob/main/4.png)

### Проверка Service
Вывод команды:

`microk8s kubectl get svc -o wide`

![netology-svc get svc](https://github.com/Furious992/k8s-1-/blob/main/5.png)

### Подключение к Service через port-forward
Команда:

`microk8s kubectl port-forward svc/netology-svc 8081:80`

Результат подключения:

![netology-svc curl](https://github.com/Furious992/k8s-1-/blob/main/6.png)
