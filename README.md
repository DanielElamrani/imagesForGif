# imagesForGif


Hi Professor,

In this repository you will find my putty session log showing my results for Task 1 and Task 2. For task 1 I uploaded a csv of song artists. You'll find this csv file 
included in the repository.

My goal was to get a report that showed the top 20 songs from that week. I trimmed the file by taking just the top 20 lines using the 
head -n "number of lines" input.csv > newFile.csv command. I now had a file of just 20 lines. I wanted to only include the Song name and artist name so I used the 
cut -d, f"number values corresponding to columns" --complement newFile.csv > trimmedNewFile.csv command to trim the csv columns and place it in a new file.  

I now had my report. 

I made a script that automatically trimmed the input csv and returned a top 20 song csv and also prints the report to the terminal. This is the script below.


[delamran@sol28 ~]$ vim scriptForTop20song.sh
cut -d, -f1,4,5 --complement songs.csv > songsReportTrimmed.csv
head -n 20 songsReportTrimmed.csv > top20songs1.csv
rm songsReportTrimmed.csv
head -n 20 top20songs1.csv


I of course made the script executable by using the chmod +x command on my script file.

With task 1 and 2 done, I started task 3. 

This was sort of annoying because I decided to make a gif using png images. The gif was going to say "Hi Prof". I unknowingly used a png file that must have been corrupted
and this caused me to do some intense googling. I eventually found the reason why I was getting an error and I replaced the image. 

For task 3 I had to find png images, put them in a repo, then clone the repo to my linux machine, use image magick to make the gif and then push the changes to my repo so the
gif would appear in my repo. I ran into a few roadblocks along the way with successfully pushing the gif to my repo but in the end I got it to work. 

The commands for the gif were

convert -dispose Previous -delay 75 -loop 0 *.png -scale 256x256

This took all of my png's and made a gif. I originally did not include the dispose command and this led to the gif having all the letters superimposed on top of eachother.
The delay command also took a bit of working with. I orginally used the value 2 which was way too fast. I read that it was in miliseconds so I tried 400 to make each
image change after .4 seconds. This did not work at all. To be honest I have no clue what the unit is but I enveutally found the value of 75 to work well.

My gif is in this repo.

Overall, I learned a lot about using the terminal and am more comfortable but I still find it to be a bit cumbersome, which I know it is the opposite of cumbersome once
you're used to it but I'm still in the early stages. 


