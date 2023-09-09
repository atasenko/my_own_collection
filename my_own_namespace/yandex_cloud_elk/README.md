# Ansible Collection - my_own_namespace.yandex_cloud_elk  

Test collection with my own module. Module can create text file with content provided.  
Role my_file_module [README](roles/my_file_module/README.md)  

# Usage  

Download [collection](../../my_own_namespace-yandex_cloud_elk-1.0.0.tar.gz)  
Run  
ansible-galaxy collection install <archivename>.tar.gz
Playbook example  

    - name: Test file module
      hosts: localhost
      collections:
        - my_own_namespace.yandex_cloud_elk
      vars:
        path: "file.txt"
        content: "Content for file"
      roles:
        - my_file_module
