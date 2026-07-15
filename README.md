# devops-netology
Привет, Нетология!

## Что игнорирует .gitignore для Terraform

Благодаря .gitignore в каталоге terraform в репозиторий не попадут служебные и секретные файлы Terraform. Это локальные папки .terraform, файлы состояния .tfstate и их резервные копии, логи падений crash.log, файлы переменных .tfvars и .tfvars.json (в них часто лежат пароли и ключи), override-файлы для локальных правок, файл блокировки .terraform.tfstate.lock.info, а также конфиги CLI (.terraformrc и terraform.rc).

Эта строка добавлена в ветке fix.
