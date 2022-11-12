# singularity container
- This is used for HPC script running
- Ideally, the `.sif` should be derived from `../docker/`. But this may take a lot of time. I think it will be more efficient to use some common `.sif` image.

## quick start
- test your docker image using the docker folder

```
cd /projects/sh-li-lab/share/SiddiqaA/Singularity_AS

# now have an interactive session on compute node
srun -p dev -q dev -N 1 -n 1 -c 2 --mem 16G --time 8:00:00 --pty bash

module load singularity

./Singularity_AS/slim2.sif jupyter-lab --no-browser --ip=$(hostname -i) --port=8884
```


## slurm read
- `https://docs.slurm.cn/users/kuai-su-ru-men-yong-hu-zhi-nan`

## singularity and Docker
- `https://docs.sylabs.io/guides/2.6/user-guide/singularity_and_docker.html`