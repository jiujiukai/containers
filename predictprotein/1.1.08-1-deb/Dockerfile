FROM biocontainers/biocontainers:vdebian-buster-backports_cv1
MAINTAINER biocontainers <biodocker@gmail.com>
LABEL    software="predictprotein" \ 
    base_image="biocontainers/biocontainers:vdebian-buster-backports_cv1" \ 
    container="predictprotein" \ 
    about.summary="suite of protein sequence analysis tools" \ 
    about.home="http://www.predictprotein.org" \ 
    software.version="1.1.08-1-deb" \ 
    upstream.version="1.1.08" \ 
    version="1" \ 
    extra.identifiers.biotools="predictprotein" \ 
    about.copyright="2010-2014 ROSTLAB" \ 
    about.license="GPL-3+" \ 
    about.license_file="/usr/share/doc/predictprotein/copyright" \ 
    extra.binaries="/usr/bin/predictprotein" \ 
    about.tags=""

USER root
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && (apt-get install -t buster-backports -y predictprotein || apt-get install -y predictprotein) && apt-get clean && apt-get purge && rm -rf /var/lib/apt/lists/* /tmp/*
USER biodocker
