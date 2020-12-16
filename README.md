# AleksandrZooLZakharov_platform
AleksandrZooLZakharov Platform repository

ДЗ 01 Настройка локального окружения. Запуск окружения. Запуск первого контейнера. Работа с kubectl.
1. Поды неймспейса kube-system используют priority-class вида system-critical. Таким образом, кластер будет всегда перезапускать такие поды. Подробнее тут. https://kubernetes.io/docs/tasks/administer-cluster/guaranteed-scheduling-critical-addon-pods/ При этом coredns & kube-proxy управляются соответственно replicaset & daemonset, a остальные поды - самой нодой.
2.* Причина, по которой Под с frontend  находился в статусе error - микросервису не хватало информации о необходимых для его работы переменных окружения. После добавления переменных окружения из манифеста для фронтенда - всё "заработало".


