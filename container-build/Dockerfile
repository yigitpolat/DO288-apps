# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent
COPY ./src ${DOCROOT}/
LABEL io.openshift.tags = 'httpd,apacke
EXPOSE 8080
RUN sed -i "/s/Listen 80/Listen 8080/g" /etc/conf/httpd.conf
RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
    chmod u=g /var/log/httpd /var/run/httpd
USER 1001
