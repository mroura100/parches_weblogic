Role Name
=========
Patch_WL12.2.1.3

Role para actualizar los parches de seguridad del WebLogic 12.2.1.3

Requirements
------------

Es necesario que el WL 12.2.1.3 este con la versión de java jdk1.8_191
Si esta en una versión anterior ejecutar el role WL12.2.1.3_update_jdk1.8.0.191

Role Variables
--------------


oracle_home: "/u01/Oracle/WL12/Middleware/Oracle_Home"

user: "orawls"

patch_dir: "/tmp/"

patch_file: "p35261722_122130_Generic.zip"

uncompress_patch_dir: "WLS_SPB_12.2.1.3.230405"



Example Playbook
----------------

Crear un playbook para llamar al role

- hosts: "{{ target }}"
  roles:
    - Patch_WL12.2.1.3
 
Ejemplo de ejecución

ansible-playbook Patch_WL12.2.1.3.yaml -e target=servidor1



