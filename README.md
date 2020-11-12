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

    # Shutdown computer
    sudo shutdown       # Shuts down the computer
    sudo shutdown +10   # In 10 minutes, start computer shutdown
    sudo shutdown 09:00 # At 09:00, start computer shutdown
    sudo shutdown -c    # Cancel scheduled computer shutdown
	sudo reboot
	
## Log ram usage
	filename=${1:-'ram.log'}
	sampleInterval=${2:-1}

	while true; 
	do
		free >> $filename;
		sleep $sampleInterval;
	done

## Check if CPU supports a given extension
	extension=$1
	grep $extension /proc/cpuinfo

## How to make bootable USB stick
1.  Find your USB stick path
> df
2.  Unmount it
> sudo umount \<Path to USB stick\>
3.  Copy data to drive
> sudo dd if=\<Path to disk image (.iso file)\> of=\<Path to USB stick\> bs=4M
4.  Now, wait...

## Change linux clock to use Local time
When dualbooting Windows and Linux, you may encounter that your clock in each OS show you different times, this happens cause Windows expects the time to be stored in Local Time and Linux at UTC, this can be fixed by changing Linux to store the current time in Local Time using:

	timedatectl set-local-rtc 1 --adjust-system-clock
