Project Description: Custom AutoInstall Apps
Why I wanted this feature: I do very frequent upgrades of my PC for both laptops and desktops and I have a few key programs that I prefer to use as my defaults, but using the default programs on Windows through Edge is a hassle because you have to find the websites and install them manually which is a huge time waster whenever you are using a new PC. This batch script aims to solve that by using a program called curl that uses the command line to find the programs and install them automatically. Not only does this solve how long it takes to find each website and download each program, but if you put it on a flash drive you can load them very quickly on client PC’s whenever you want to diagnose an issue and want to browse with comfortable settings; or you could run it on virtual machines to have all your base programs all in one place. 
What you need (All of this should be included in the linked GitHub)
Curl (can be found at https://curl.se/windows/ or can be downloaded in the files)
File Archiver Software like WinZip, WinRAR, or an equivalent program
A program to create and edit batch files (Notepad++ is what I used but others should work)
Optional: Having either an external storage device or a cloud drive such as Dropbox or Google Drive would be helpful but not required
1: Download curl using either the link above or in the files posted
2: Create a folder in your desired place and extract the downloaded program in that folder
3: Press the Win Key and type “Environment Variables” until “Edit the system environment variables” appears in the Search, then click on the option

4: In the System Properties window; select the “Environment Variables” option; then select New on either user or system variables. Then under the “Variable Name” option, add the path to the folder you created for curl; then add the “Variable Name” you want and select OK on both windows to save your changes.


5: To check if you did it successfully, go to the command line and type curl –version. If done correctly, the command line should output something that looks like this: 



6: Next, open up your text editing program of choice and create a new text file. Then copy and paste this template:
@echo off
echo Downloading all programs...

curl -L -o program1.exe https://example.com/program1.exe
curl -L -o program2.exe https://example2.com/program2.exe
curl -L -o program3.exe https://example3.com/program3.exe

echo Downloads are completed.
Pause
For the program, you will need to replace the executable name (shown in blue for clarity) with the name of the file you want to download, and the source website with where the file link you want to use for the download is (shown in green for clarity). To get the link from a button on the website easier, you can right click the link, and select “Copy Link Address” in the options like this: 
 
7: Save your file as a Batch (.bat) file in your desired location.
8: To test the script, click on the file and run the script. If successful, your command prompt should look like this and the file downloaded should appear in the same folder where the batch script is located: 


9: Close command prompt and enjoy your new programs 😉
Helpful Tips: 
-	You can also install curl more quickly by directly using the command line by typing this into the command prompt: setx <variable_name> "<variable_value>". 


