Alfresco-EditOnline4.2.c-fix
============================

AMP for Alfresco Share 4.2.c to fix the broken "Edit Online" button

Install
=======

    java -jar /path/to/alfresco-mmt.jar install alfresco-editonline42c-fix.amp /path/to/share.war -force

We need the -force option because this amp overwrites Alfresco's base Javascript files. Don't worry, they get backed up and you can revert to them by uninstalling the amp:

Uninstall
=========

    java -jar /path/to/alfresco-mmt.jar uninstall org.alfresco.fix.editonline42c /path/to/share.war

"Build" from source
===================

It's not worth making an ant or maven file, really - the amp is just a zipped version of the src/ directory that you can regenerate with:

    cd src/
    zip -rv ../alfresco-editonline42c-fix.amp ./*


