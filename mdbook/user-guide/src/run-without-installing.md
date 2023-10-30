# Run without installing


## Run from Flakehub

[![FlakeHub](https://img.shields.io/endpoint?url=https://flakehub.com/f/so-dang-cool/dt/badge)](https://flakehub.com/flake/so-dang-cool/dt)

Add dt to your `flake.nix`:

```nix
{
  inputs.dt.url = "https://flakehub.com/f/so-dang-cool/dt/*.tar.gz";

  outputs = { self, dt }: {
    # Use in your outputs
  };
}

```

## Run from Docker

An ***experimental*** Docker container is available:

* https://hub.docker.com/r/booniepepper/dt

Pull:

```
$ docker pull booniepepper/dt
```

REPL

```
$ docker run -it booniepepper/dt ''
dt 1.x.x
Learn from my mistakes - someone should.
» 
```

Pipe

```
❯ seq 5 | docker run -i booniepepper/dt '[\n: ["*" print] n times nl] each'
*
**
***
****
*****
```

