# Custom-Program-Downloader
# Uses a batch script combined with curl to download programs automatically on a PC using the command prompt
@echo off
echo Downloading multiple programs...

curl -L -o program1.exe https://example.com/program1.exe
curl -L -o program2.exe https://example2.com/program2.exe
curl -L -o program3.exe https://example3.com/program3.exe

echo Download completed.
pause
