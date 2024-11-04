# Terraform para Azure: Creación de una Máquina Virtual con Windows Server 2022

Este proyecto utiliza Terraform para crear una máquina virtual en Azure con Windows Server 2022, un disco de datos de 512 GB y una IP pública en la región de Canadá Central.

## Requisitos

- [Terraform](https://www.terraform.io/downloads.html) instalado en tu máquina.
- Una cuenta de Azure con los permisos necesarios para crear recursos.

## Configuración

1. Clona este repositorio o copia los archivos en tu máquina local.
2. Asegúrate de tener configuradas tus credenciales de Azure. Puedes hacerlo utilizando el comando `az login` de la CLI de Azure.

## Uso

1. Inicializa el proyecto de Terraform:

    ```sh
    terraform init
    ```

2. Revisa el plan de ejecución para asegurarte de que los recursos se crearán según lo esperado:

    ```sh
    terraform plan
    ```

3. Aplica el plan para crear los recursos en Azure:

    ```sh
    terraform apply
    ```

    Se te pedirá que confirmes la ejecución. Escribe `yes` y presiona Enter.

## Recursos Creados

Este proyecto creará los siguientes recursos en Azure:

- Un grupo de recursos (`azurerm_resource_group`)
- Una red virtual (`azurerm_virtual_network`)
- Una subred (`azurerm_subnet`)
- Una IP pública (`azurerm_public_ip`)
- Una interfaz de red (`azurerm_network_interface`)
- Una máquina virtual con Windows Server 2022 (`azurerm_virtual_machine`)

## Limpieza

Para eliminar los recursos creados por este proyecto, ejecuta:

```sh
terraform destroy
