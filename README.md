1c-web
=========

Роль осуществляет публикацию баз 1с на web-сервере/

Требования
------------
Установленный сервер 1с с базой данных

Переменные
--------------

Адрес сервера 1с:

erp_fqdn: erp.local

Название базы данных Документооборот:

docmng_base: docmng_test

Название базы данных ERP:

erp_base: erp_test

Путь публикации ERP:

erp_path: erp

Путь публикации Документооборот:

docmng_path: docmng

Пример playbook
--------------
```
- name: Configure 1c-web
  hosts: erp
  become: true
  vars:
    erp_fqdn: lc-erp-test.local
    docmng_base: docmng_base
    erp_base: erp_base
    erp_path: erp
    docmng_path: docmng

  roles:
    - 1c-web
```
