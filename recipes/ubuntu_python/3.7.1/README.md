### The Stack is based on [`eclipse/stack-base`](https://hub.docker.com/r/eclipse/stack-base/) and contains
- `Python 3.7.1`
- `pip 18.1`
- `Ubuntu 16.04`

### Example configuration
On [`GitHub`](https://github.com/maxsid/che-dockerfiles/blob/master/examples/ubuntu_python/3.7.1/raw-configuration.json)

```json
{
  "description": "Default Python Stack with Python 3.7.1, pip 18.1.",
  "scope": "general",
  "tags": [
    "pip",
    "Python 3.7.1"
  ],
  "creator": "b07e3a58-ed50-4a6e-be17-fcf49ff8b242",
  "workspaceConfig": {
    "environments": {
      "default": {
        "recipe": {
          "type": "dockerimage",
          "content": "maxsid/ubuntu_python:3.7.1"
        },
        "machines": {
          "dev-machine": {
            "env": {},
            "installers": [
              "org.eclipse.che.exec",
              "org.eclipse.che.terminal",
              "org.eclipse.che.ws-agent",
              "org.eclipse.che.ls.python"
            ],
            "volumes": {},
            "servers": {
              "8080/tcp": {
                "attributes": {},
                "protocol": "http",
                "port": "8080"
              },
              "8000/tcp": {
                "attributes": {},
                "protocol": "http",
                "port": "8000"
              }
            },
            "attributes": {
              "memoryLimitBytes": "2147483648"
            }
          }
        }
      }
    },
    "projects": [],
    "defaultEnv": "default",
    "commands": [
      {
        "commandLine": "cd ${current.project.path} && python main.py",
        "name": "run",
        "type": "custom",
        "attributes": {
          "goal": "Run",
          "previewUrl": ""
        }
      }
    ],
    "name": "default",
    "attributes": {},
    "links": []
  },
  "components": [
    {
      "version": "16.04",
      "name": "Ubuntu"
    },
    {
      "version": "3.7.1",
      "name": "Python"
    },
    {
      "version": "18.1",
      "name": "PIP"
    }
  ],
  "name": "Python-3.7.1",
  "id": "stack0scsoswa3l79o750"
}
```

### Links
- [`Eclipse Che`](https://eclipse.org/che/)
- [`eclipse/stack-base`](https://hub.docker.com/r/eclipse/stack-base/)
