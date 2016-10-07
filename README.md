# telemac-docker
opentelemac on docker

# quick start
    docker run -i -t -P ubuntu /bin/bash
    apt-get update
    apt-get install -y build-essential gfortran subversion python nano
    
    mkdir v6p3r2 && cd v6p3r2
    
    svn co http://svn.opentelemac.org/svn/opentelemac/tags/v6p3r2/builds
     username: ot-svn-public
     password: telemac1*
    svn co http://svn.opentelemac.org/svn/opentelemac/tags/v6p3r2/configs
    svn co http://svn.opentelemac.org/svn/opentelemac/tags/v6p3r2/scripts
    svn co http://svn.opentelemac.org/svn/opentelemac/tags/v6p3r2/sources
    
    export PATH=/v6p3r2/scripts/python27:$PATH
    export SYSTELCFG=/v6p3r2/configs/systel.cis-ubuntu.cfg
    
    nano $SYSTELCFG
     edit the 
    compileTELEMAC.py
    
