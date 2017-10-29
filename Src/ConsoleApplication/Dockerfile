FROM microsoft/windowsservercore

SHELL ["powershell"]

# Note: Add NuGet
RUN Invoke-WebRequest "https://dist.nuget.org/win-x86-commandline/latest/nuget.exe" -OutFile "C:\windows\nuget.exe" -UseBasicParsing  


# Note: Install Web Targets
RUN &  "C:\windows\nuget.exe" Install NUnit -OutputDirectory packages

ADD bin/debug /
ENTRYPOINT ConsoleApp2.exe
