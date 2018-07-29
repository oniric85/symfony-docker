FROM httpd:2.4

COPY httpd-vhosts.conf /usr/local/apache2/conf/extra/httpd-vhosts.conf

RUN sed -i '/Include conf\/extra\/httpd-vhosts\.conf/s/^#//g' /usr/local/apache2/conf/httpd.conf \
    && sed -i '/LoadModule proxy_module/s/^#//g' /usr/local/apache2/conf/httpd.conf \
    && sed -i '/LoadModule proxy_fcgi_module/s/^#//g' /usr/local/apache2/conf/httpd.conf

EXPOSE 80