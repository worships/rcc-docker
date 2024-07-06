# RCCService Linux Image Docker Implementation

FROM debian:stable-slim

RUN dpkg --add-architecture i386 && \
    apt-get update && \
    apt-get install -y wine32 wget && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /RCC
COPY RCC /RCC

# SOAP Server Port
EXPOSE 64989
# Game UDP Ports
EXPOSE 53640-53900

CMD ["wine", "RCCService.exe", "-Console", "-verbose", "-port", "64989"]