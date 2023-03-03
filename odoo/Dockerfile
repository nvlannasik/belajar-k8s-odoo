FROM arm32v7/python:3.9-buster

RUN apt-get update && \
    apt-get install -y \
        python3-dev \
        build-essential \
        libpq-dev \
        libjpeg-dev \
        libxml2-dev \
        libxslt1-dev \
        libldap2-dev \
        libsasl2-dev \
        libffi-dev \
        libssl-dev \
        libfontconfig1 \
        libfreetype6 \
        libx11-6 \
        libxext6 \
        wget \
        curl

RUN wget -O - https://nightly.odoo.com/odoo.key | apt-key add -
RUN echo "deb http://nightly.odoo.com/14.0/nightly/deb/ ./" >> /etc/apt/sources.list.d/odoo.list
RUN apt-get update && \
    apt-get install -y odoo

EXPOSE 8069

CMD ["odoo"]