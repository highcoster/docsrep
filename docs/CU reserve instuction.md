# Инструкция по резервированию модуля CU

Для создания резервной копии CU выполнить следующие шаги:

1. Авторизоваться на сервере CU как devops, для этого открыть терминал и выполнить _ssh devops@10.5.5.111.
2. Перейти в папку enb_package, для этого выполнить в терминале cd/mnt/x86_cu/enb_package.
3. Выполнить в терминале:

ansible-playbook \
playbooks/enb_backup.yml \
-i inventory_tele2/bbu_nn000659.yaml \
-i inventory_tele2/bbu_nn000692.yaml \
-i inventory_tele2/bbu_nn000727.yaml \

В результате, в папке /tmp будет создан файл _vran_backup_<временная метка>.tar.gz_ с резервной конфигурацией.
