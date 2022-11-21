FROM  mcr.microsoft.com/devcontainers/base:jammy

RUN apt-get update \
    && apt-get install --no-install-recommends -y rsyslog systemd systemd-cron \
    # Fix a bug with common-debian script
    && rm -f /usr/local/bin/systemctl \
    #  Clean up
    && apt-get clean && rm -rf /var/lib/apt/lists/*

CMD ["/lib/systemd/systemd", "--system", "--unit=basic.target"]