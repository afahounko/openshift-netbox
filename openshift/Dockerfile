FROM python-s2i

USER 0

RUN mv $STI_SCRIPTS_PATH/assemble $STI_SCRIPTS_PATH/assemble-base
COPY s2i/assemble.sh $STI_SCRIPTS_PATH/assemble
COPY s2i/run.sh $STI_SCRIPTS_PATH/run
RUN chmod +x $STI_SCRIPTS_PATH/*

COPY netbox/settings.py /opt/app-root/etc/settings.py

USER 1001

