# Userful-Linux-Commands

## Replace Name/Ext

> ls | cat -n | while read n f; do mv "$f" "$n.ext"; done

Where:
    
    n is a number (0, 1, 2 ...)
  
    f is the file name (folder, a.png, d.txt)
  
## Tar
    tar -czf  file.tar.gz dir
    tar -ztvf file.tar.gz
    tar -xvzf file.tar.gz
    
| Option | Description                     |
|--------|---------------------------------|
| -t     | list                            |
| -x     | extrct                          |
| -v     | verbose list                    |
| -f     | file                            |
| -z     | Compress/Decompress Gzip - gz   |
| -j     | Compress/Decompress Bzip2 - bz2 |

## Jupyter Lab with Conda Env
    conda install ipykernel
    ipython kernel install --user --name=<env_name>

## Jupyter Lab with TQDM

    pip install ipywidgets 
    conda install -c conda-forge nodejs 
    jupyter nbextension enable --py widgetsnbextension
    jupyter labextension install @jupyter-widgets/jupyterlab-manager

## Check NVIDIA Memory Usage / CUDA / CUDNN

    watch -n 0.5 nvidia-smi
    whereis cuda
    cat /usr/local/cuda/version.txt
    nvcc --version
    cat /usr/local/cuda/include/cudnn.h | grep CUDNN_MAJOR -A 2

## Shell Commands

	> # Command to overwrite to a file
	>> # Command to append to a file
	echo rapela > out.txt
	echo rapela >> out.txt

	sudo shutdown
	sudo reboot