FROM unicon/simplesamlphp@sha256:6daff6f7ea8dcf24fdb937906388b0af5dadbf20276086ab22fd8b7b9b9201db

RUN yum -y update \
    && yum -y install php55w-ldap \
    && yum -y clean all

COPY etc-httpd /etc/httpd/
COPY var-simplesamlphp /var/simplesamlphp/
COPY var-www-html/ /var/www/html/

RUN chown apache:apache /var/simplesamlphp/log/ \
    && chown -R apache:apache /var/simplesamlphp/cert/
