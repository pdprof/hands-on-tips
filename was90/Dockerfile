FROM ibmcom/websphere-traditional:9.0.5.10
ENV ENABLE_BASIC_LOGGING=true
COPY PASSWORD /tmp/PASSWORD
COPY --chown=was:root virtual-host.py /work/config/
RUN /work/configure.sh
