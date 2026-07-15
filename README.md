# devops-netology
Привет, Нетология!

## Что игнорирует .gitignore для Terraform

Ниже расшифровка правил из terraform/.gitignore, то есть какие имена файлов под них попадают. Звёздочка * означает любой набор символов, а ** означает любой уровень вложенности папок.

- `**/.terraform/*` : всё содержимое папок с именем .terraform на любом уровне вложенности
- `*.tfstate` : любые файлы с расширением .tfstate
- `*.tfstate.*` : файлы, где после .tfstate стоит ещё точка и что угодно, например terraform.tfstate.backup
- `crash.log` : файл ровно с именем crash.log
- `crash.*.log` : файлы вида crash.что-угодно.log
- `*.tfvars` : любые файлы с расширением .tfvars
- `*.tfvars.json` : любые файлы, оканчивающиеся на .tfvars.json
- `override.tf` и `override.tf.json` : файлы ровно с такими именами
- `*_override.tf` и `*_override.tf.json` : файлы, имя которых оканчивается на _override.tf или _override.tf.json, в начале может быть что угодно
- `.terraform.tfstate.lock.info` : файл ровно с этим именем
- `.terraformrc` и `terraform.rc` : файлы ровно с такими именами

Строки, которые начинаются с #, это комментарии, они ничего не игнорируют.
