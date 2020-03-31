# Userful-Linux-Commands

## Replace Name/Ext

> ls | cat -n | while read n f; do mv "$f" "$n.ext"; done

Where:
    
    n is a number (0, 1, 2 ...)
  
    f is the file name (folder, a.png, d.txt)
  
## Tar
    tar -xzvf file.tar.gz
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

