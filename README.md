.terraform/	Игнорирует папку с именем .terraform (и всё внутри неё)	.terraform/, .terraform/plugins/...
*.tfstate	Любой файл, заканчивающийся на .tfstate	terraform.tfstate, dev.tfstate
*.tfstate.*	Любой файл вида что‑то.tfstate.что‑то	terraform.tfstate.backup, prod.tfstate.123
crash.log	Только файл с точным именем crash.log	crash.log (но не crash_2025.log)
crash.*.log	Файлы, начинающиеся с crash., затем любой текст, затем .log	crash.1.log, crash.debug.log
*.tfvars	Любой файл с расширением .tfvars	prod.tfvars, secrets.tfvars
*.tfvars.json	Любой файл с суффиксом .tfvars.json	config.tfvars.json, vars.tfvars.json
override.tf	Только файл override.tf	override.tf (не my_override.tf)
override.tf.json	Только файл override.tf.json	override.tf.json
*_override.tf	Любой файл, который заканчивается на _override.tf	local_override.tf, dev_override.tf
*_override.tf.json	Любой файл, который заканчивается на _override.tf.json	test_override.tf.json
.terraform.tfstate.lock.info	Только этот конкретный файл	.terraform.tfstate.lock.info (никакие другие)
.terraformrc	Только файл .terraformrc	.terraformrc
terraform.rc	Только файл terraform.rc	terraform.rc
Строки, начинающиеся с #, — это комментарии, Git их игнорирует.

Строка вида !example_override.tf — это исключение: она отменяет игнорирование для конкретного файла, даже если он попадает под другие правила.
