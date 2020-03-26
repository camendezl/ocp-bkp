# Playbook para la toma de backups de un cluster de OCP 3.11
Este playbook fue desarrollado siguiendo las recomendaciones de la documentación oficinal disponible en https://docs.openshift.com/container-platform/3.11/day_two_guide/environment_backup.html. Tenga en cuenta que solo se realiza respaldo de lo documentado, y las aplicaciones o datos asociados a ellas deberán respaldarse mediante otro método.


Para ejecutarlo, ubique el playbook y los roles en la misma carpeta dentro del servidor bastion del clúster de OCP. Luego, ejecute:

ansible-playbook openshift_bkp.yaml

Al finalizar la ejecución del playbook, todos los respaldos estarán comprimidos en formato tar.gz organizados por host dentro de carpeta backup (que en caso que no exista previamente) será creada en la mis ubicación donde se encuentra el playbook.
