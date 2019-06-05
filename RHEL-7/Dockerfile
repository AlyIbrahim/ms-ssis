FROM registry.redhat.io/rhel7
RUN curl -o /etc/yum.repos.d/mssql-server.repo https://packages.microsoft.com/config/rhel/7/mssql-server-2017.repo
RUN yum install -y mssql-server-is
ADD ssis.conf /var/opt/ssis/ssis.conf
RUN /opt/ssis/bin/ssis-conf setup
ENV PATH=/opt/ssis/bin:$PATH
EXPOSE 1433
