# demo_teleport
archivos de configuración para **Teleport** e información adicional.

```
teleport
├── docker-compose.yml
├── node
│   ├── Dockerfile
│   └── teleport.yaml
└── server
    ├── Dockerfile
    └── teleport.yaml

3 directories, 5 files
```

- `teleport.yaml` : Guardar este archivo de configuración en **/etc/teleport.yaml** .
  
- En **/var/lib/teleport** se incluyen los datos internos del clúster: certificados, estado del clúster, usuarios, sesiones, claves.
