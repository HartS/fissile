## fissile build layer compilation

Builds a docker image layer to be used when compiling packages.

### Synopsis



This command creates a container with the name `<repository>-cbase-<FISSILE_VERSION>` 
and runs a compilation prerequisites script within. 

Once the prerequisites script completes successfully, an image named 
`<repository>-cbase:<FISSILE_VERSION>` is created and the created container is 
removed.

If the prerequisites script fails, the container is not removed. 
If the compilation base image already exists, this command does not do anything.
	

```
fissile build layer compilation
```

### Options

```
  -D, --debug   If specified, the docker container used to build the layer won't be destroyed on failure.
```

### Options inherited from parent commands

```
  -c, --cache-dir string         Local BOSH cache directory. (default "~/.bosh/cache")
      --config string            config file (default is $HOME/.fissile.yaml)
  -f, --configgin string         Path to the tarball containing configgin.
  -d, --dark-opinions string     Path to a BOSH deployment manifest file that contains properties that should not have opinionated defaults.
  -F, --from string              Docker image used as a base for the layers (default "ubuntu:14.04")
  -l, --light-opinions string    Path to a BOSH deployment manifest file that contains properties to be used as defaults.
  -N, --no-build                 If specified, the Dockerfile and assets will be created, but the image won't be built.
  -o, --output string            Choose output format, one of human, json, or yaml (currently only for 'show properties') (default "human")
  -r, --release string           Path to dev BOSH release(s).
  -n, --release-name string      Name of a dev BOSH release; if empty, default configured dev release name will be used
  -v, --release-version string   Version of a dev BOSH release; if empty, the latest dev release will be used
  -p, --repository string        Repository name prefix used to create image names. (default "fissile")
  -m, --role-manifest string     Path to a yaml file that details which jobs are used for each role.
  -w, --work-dir string          Path to the location of the work directory. (default "/var/fissile")
  -W, --workers int              Number of workers to use. (default 2)
```

### SEE ALSO
* [fissile build layer](fissile_build_layer.md)	 - Has subcommands for building Docker layers used during the creation of your images.

###### Auto generated by spf13/cobra on 25-Oct-2016
