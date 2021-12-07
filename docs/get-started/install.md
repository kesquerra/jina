(install)=
# Install

Standard install enables the full features of Jina. 

#### via PyPI
>```shell
>pip install -U jina
>```
#### via Conda
>```shell
>conda install jina -c conda-forge
>````
#### via Docker
>```shell
>docker run jinaai/jina:latest
>```

## More install options

Version identifiers [are explained here](https://github.com/jina-ai/jina/blob/master/RELEASE.md).

### Minimum

Minimum install enables basic features of Jina, but without support for HTTP, WebSocket, Docker and Hub.

Minimum install is often used when building and depolying an Executor.


#### via PyPI

>```shell
>JINA_PIP_INSTALL_CORE=1 pip install jina
>```

#### via Conda

>```shell
>conda install jina-core -c conda-forge
>```

#### via Docker

>```shell
>docker run jinaai/jina:latest
>```

### Minimum but more performant

Same as minimum install, but also install `uvloop` and `lz4`.


#### via PyPI

>```shell
>JINA_PIP_INSTALL_PERF=1 pip install jina
>```


#### via Conda

>```shell
>conda install jina-perf -c conda-forge
>```

#### via Docker

>```shell
>docker run jinaai/jina:latest-perf
>```


### With Daemon (JinaD)

Same as minimum install, but also install `uvloop` and `lz4`.

>```shell
>pip install "jina[daemon]"
>```


### Full development dependencies


#### via PyPI

>```shell
>pip install "jina[devel]"
>```


#### via Docker

>```shell
>docker run jinaai/jina:latest-devel
>```


### Prerelease

Prerelease is the version always synced with the `master` branch of Jina's GitHub repository.

#### via PyPI

>```shell
>pip install --pre jina
>```


#### via Docker

>```shell
>docker run jinaai/jina:master
>```





## Autocomplete commands on Bash, Zsh and Fish

After installing Jina via `pip`, you should be able to use your shell's autocomplete feature while using Jina's CLI. For example, typing `jina` then hitting your Tab key will provide the following suggestions:

```bash

jina 

--help          --version       --version-full  check           client          flow            gateway         hello-world     log             pea             ping            pod
```

The autocomplete is context-aware. It also works when you type a second-level argument:

```bash

jina pod --name --lo

--log-profile  --log-remote   --log-sse
```


Currently, the feature is enabled automatically on Bash, Zsh and Fish. It requires you to have a standard shell path as follows:

| Shell | Configuration file path      |
| ---   | ---                          |
| Bash  | `~/.bashrc`                  |
| Zsh   | `~/.zshrc`                   |
| Fish  | `~/.config/fish/config.fish` |

