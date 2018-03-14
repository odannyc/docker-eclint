# docker-eclint
A Docker Image to run [editorconfig](http://editorconfig.org/) checks using [eclint](https://github.com/jedmao/eclint)

## Usage
To use you have to simply have a `.editorconfig` file in the root of your project and run:

```
docker run --rm -v $(pwd):/app/code odannyc/eclint check
```

That will pull down the `odannyc/eclint` image from dockerhub, then run the `check` command from eclint.

The `--rm` option is used to remove the container when the command is done executing and the `-v $(pwd):/app/code` option will take your current directory and share it as a volume within the container (so make sure you run the docker from the root of your project).
