# telemac-docker
opentelemac on docker

# quick start
    docker run -i -t -p 8000:8000 ubuntu /bin/bash
    
    apt-get update && apt-get install -y build-essential gfortran subversion python nano python-pip
    
    mkdir v6p3r2 && cd v6p3r2
    
    svn co http://svn.opentelemac.org/svn/opentelemac/tags/v6p3r2/builds
     ## username: ot-svn-public
     ## password: telemac1*
    svn co http://svn.opentelemac.org/svn/opentelemac/tags/v6p3r2/configs
    svn co http://svn.opentelemac.org/svn/opentelemac/tags/v6p3r2/scripts
    svn co http://svn.opentelemac.org/svn/opentelemac/tags/v6p3r2/sources
    
    cd /
    
    export PATH=/v6p3r2/scripts/python27:$PATH
    export SYSTELCFG=/v6p3r2/configs/systel.cis-ubuntu.cfg
    
    nano $SYSTELCFG
     ## edit the file contents to match the on on this repo
    
    compileTELEMAC.py
    
    pip install wooey
    
    wooify -p opentelemac
    
    cd opentelemac/
    python manage.py createsuperuser # and follow instructions
    python manage.py runserver 0.0.0.0:8000

And finally visit below link from the host browser

http://localhost:8000/admin
