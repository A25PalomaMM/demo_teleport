# demo_teleport
Repo con archivos de configuración para **Teleport**. 

La carpeta `/docker` incluye los archivos para probar el escenario con Docker, y las carpetas `/node` y `/server` contienen los archivos para probarlo en máquinas virtuales Linux que recomienda Teleport(Ubuntu 16.04+, Debian 9+).
[Consultar aquí la documentación oficial de Teleport:](https://goteleport.com/docs/connect-your-client/teleport-clients/tsh/)

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
