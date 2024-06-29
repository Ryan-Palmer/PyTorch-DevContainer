# Pytorch DevContainer template

To run on Windows you will need:

- An Nvidia GPU with latest drivers installed
- Docker Desktop
- WSL2
- VSCode with the DevContainers extension

## Dependencies

### Ubuntu
If you need to `apt-get` any apps, add them to the Dockerfile where indicated.

### Python
Add any pip packages you need to pip-packages.txt before building the container.

## Build and Run
To build and launch the VSCode and Jupyter servers in a dev container, open the command pallete and run `Dev Containers: Reopen in Container`.

Once it has finished launching then VSCode should auto-select the Jupyter Python kernel and prompt you for the Jupyter password, which is `dev`.

> This can be changed in the Docker file or ommitted completely to force Jupyter to create a new GUID key which be displayed along with the server URL in the terminal.

If it doesn't do this automatically, set the kernel of your Polyglot Notebooks session to `http://127.0.0.1:8888/lab?token=dev`.

You can also visit that URL in your browser if you would rather use the Jupyter Labs IDE.

> If you see some errors about the .NET SDK version and Python Kernel being invalid after first launch, don't worry, the installer is just catching up. You don't need to install anything.


## Workspace files
Any files you put in the `src` folder will be available to the Docker container and the Jupyter server.

### Adding VSCode extensions
After you launch the DevContainer you can select extensions in VSCode, click their settings cog and select "Add to `devcontainer.json`".

Once you have done this for all the extensions you need, open the command pallete and run `Dev Containers: Rebuild and Reopen in Container`.