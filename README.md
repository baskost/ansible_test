#ansible_test

1. Ansible запускаем из виртуального окружения:
mkdir ansible-netbox
cd ansible-netbox/
python3 -m venv .
source bin/activate

Устанавливаем Ansible и компоненты:
python3 -m pip install --upgrade pip
pip install pynetbox
pip install ansible
pip install netaddr
pip install pytz
ansible-galaxy collection install netbox.netbox
ansible-galaxy collection install cisco.ios


2. Проверка создания инвентаря из NetBox: ansible-inventory --list -i netbox_inv.yml

3. Запуск плейбука: ansible-playbook backup_sw.yml
