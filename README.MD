# Задание
Написать playbook, который подготавливает сборочное и продовое окружение на двух нодах. На сборочной ноде производится сборка проекта, на продовой - запуск.


## Памятка по командам
### Линтеры
```bash
apt install yamllint ansible-lint
yamllint git-checkout-ang-package.yml
ansible-lint git-checkout-ang-package.yml
```
### Запуск
```bash
ansible-playbook build_and_deployment.yml -i ./hosts
ansible-playbook git-checkout-ang-package.yml -i ./hosts
```


## TODO
* [x] Можно ли файл `hosts` положить рядом в проект? Будет ли он браться в приоритете над файлом `/etc/ansible/hosts`?
* [x] Научиться получать исходники приложения на сборочном сервере
* [ ] Научиться сохранять результаты сборки в каком-нибудь хранилище, вроде это `ansible-galaxy`
* [ ] Научиться получать артефакт сборки на продовой машине