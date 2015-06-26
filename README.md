Example ${jetty.base} with custom connectors
============================================

This is a Jetty 9.2+ ${jetty.base} showing how to setup
custom Connectors for a specific instance of Jetty.

Looking at the `start.ini` you will see that there is
no reference to `--module=http` or `--module=https`
as we are setting up our own custom connectors in
this specific case.

The setup:
----------

4 total connectors

     Port  |  Role                |  Name      | Defined In
    -------+----------------------+------------+-------------------------
     8080  |  Plain HTTP          | conn-app1  | etc/app1-connectors.xml
     8443  |  HTTP/1.1 over SSL   | conn-app1  | etc/app1-connectors.xml
     9600  |  Plain HTTP          | conn-app2  | etc/app2-connectors.xml
     9601  |  HTTP/1.1 over SSL   | conn-app2  | etc/app2-connectors.xml


