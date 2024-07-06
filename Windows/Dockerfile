# RCCService Windows Image Docker Implementation

FROM mcr.microsoft.com/windows/servercore:ltsc2019

WORKDIR /RCC
COPY RCC /RCC

# SOAP Server Port
EXPOSE 64989
# Game UDP Ports
EXPOSE 53640-53900

CMD ["cmd", "/c", "RCCService.exe -Console -verbose -port 64989"]