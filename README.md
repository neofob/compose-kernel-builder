Build the kernel from source with gcc container
===============================================
*A container to build linux kernel with the latest gcc*.

Required stuff
=============
* Linux Kernel Source [`code`][3], check out locally
* `docker-compose`

WorkFlow
========
```
$ git clone git://git.kernel.org/pub/scm/linux/kernel/git/stable/linux-stable.git
$ cd linux-stable
$ git checkout linux-4.18.y
# or your branch/commit
# cd back to this directory
# edit default_settings.env to point correct places

$ docker-compose build
$ docker-compose up
```

Default Environment Variables
=============================
| Variable       | Default Value |
|:--------------:|:-------------:|
| `KERNEL_SRC`   | `/src/linux`  |
| `BUILD_OUTPUT` | `/tmp/`       |
| `OLD_CONFIG`   | `/tmp/old_config` |

**References:**
* [`KernelBuild`][0] from [`kernelnewbies`][1]
* [`build_kernel.sh`][2] script

__author__: *tuan t. pham*


[0]: https://kernelnewbies.org/KernelBuild
[1]: https://kernelnewbies.org
[2]: https://github.com/neofob/tscripts/blob/master/misc/build_kernel.sh
[3]: git://git.kernel.org/pub/scm/linux/kernel/git/stable/linux-stable.git
