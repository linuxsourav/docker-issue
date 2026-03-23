docker issue and resolving issue



1.problem

sourav@sourav-HP-Notebook:~$ docker run centos:latest
Unable to find image 'centos:latest' locally
docker: Error response from daemon: failed to resolve reference "docker.io/library/centos:latest": docker.io/library/centos:latest: not found

Run 'docker run --help' for more information

solution

That error is actually expected — nothing is “wrong” with your Docker setup 👍

❗ Why this happens

The image centos:latest no longer exists on Docker Hub.

CentOS changed its direction to CentOS Stream, and the official latest tag was removed. So Docker cannot find it.

we can run 

---- docker pull centos:centos7.9.2009 -----
