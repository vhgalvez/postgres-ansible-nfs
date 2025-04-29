# 📦 Proyecto Ansible - PostgreSQL con NFS en AlmaLinux

Este proyecto automatiza la instalación de Docker y el despliegue de PostgreSQL en AlmaLinux 9, usando almacenamiento persistente montado por NFS desde un servidor Flatcar Linux.

## 🚀 Ejecución

```bash
ansible-playbook -i inventory/hosts.ini playbooks/install_postgres_nfs.yml
```

## ✅ Requisitos

- El servidor Flatcar debe exportar `/srv/nfs/postgresql` vía NFS.
- En AlmaLinux, debe instalarse `nfs-utils`.
- Las claves SSH deben estar correctamente configuradas.

## Estructura

- `roles/docker_setup/`: Instala Docker y el plugin Compose.
- `roles/nfs_mount/`: Monta el volumen NFS.
- `roles/postgres_deploy/`: Despliega PostgreSQL usando docker-compose.

