FROM v8tix/cronov:0.0.4.v20200324.0efd158
LABEL MAINTAINER="V8TIX"
LABEL MAIL="info@v8tix.com"
ADD packages /home/packages
RUN ["/bin/bash", "-c", "chmod +x -R /home/packages"]
RUN ["/bin/bash", "-c", "/home/packages/packages.sh"]
RUN ["/bin/bash", "-c", "/home/v8tix/libraries/zemni/system/sec/remove_all_perm.sh"]
RUN ["/bin/bash", "-c", "/home/v8tix/libraries/zemni/system/cleanup/cleanup.sh"]
USER v8tix:v8tix
ADD --chown=v8tix:v8tix entrypoint /home/v8tix/entrypoint
ENTRYPOINT ["/home/v8tix/entrypoint/entrypoint.sh"]