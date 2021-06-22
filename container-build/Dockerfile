# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent
EXPOSE 8080
LABEL io.k8s.description="A basic Apache HTTP Server child image, uses ONBUILD" \
      io.k8.display-name="Apache HTTP Server" \
      io.openshift.expose-services="8080:https" \
      io.openshift.tags="apache, http"
RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
    chmod -R g=u /var/logs/httpd /var/run/httpd
USER 1001 
