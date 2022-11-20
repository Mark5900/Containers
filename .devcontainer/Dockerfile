ARG PWSHVERSION=lts
FROM mcr.microsoft.com/powershell:${PWSHVERSION}-ubuntu-18.04

LABEL Name=containers Version=0.0.1
SHELL ["pwsh", "-noninteractive", "-command"]

RUN apt update && apt install -y git && apt clean;
RUN $ErrorActionPreference='Stop'; $ProgressPreference = 'silentlyContinue';\
    Install-Module -Name Pester -Force; \
    Install-Module -Name ExchangePowerShell -Force;