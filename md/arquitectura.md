La arquitectura de Ansible se centra en la ejecución remota de módulos en los nodos a través de SSH, utilizando playbooks y roles para organizar y estructurar la automatización

![Arquitectura](/img/arquitectura.png)

Dentro de la arquitectura de Ansible podemos encontrar diferentes componentes:

- **Control Node:** Es el sistema desde el cual se ejecutan los comandos de Ansible. En este nodo, se almacenan los playbooks, roles y el inventario.
- **Módulos:** Son considerados las unidades de trabajo en Ansible. Se basan en pequeños programas escritos en Python u otro lenguaje, con una tarea específica, que ejecuta(por SSH normalmente) y luego borra
- **Inventario:** Aquí es donde se representan las máquinas que gestionan el servicio, pudiendo elegir a qué grupo pertenece cada una de ellas.
- **Plugins:** Aportan funcionalidades extra a los módulos. Los plugins son la base de Ansible; mientras los módulos se ejecutan en los sistemas, éstos se ejecutan sobre los nodos.
- **Playbooks:** Son archivos YAML con las instrucciones de la topología del sistema. Cada Playbook sirve para asociar un grupo de hosts con un rol específico
