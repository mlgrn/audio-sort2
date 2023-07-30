# Sort Audio By RMS

## Background
I made this for making sample packs and other collections of sounds used in music production. 

You can automatically cut long recordings by transient or gate events inside a DAW like Reaper or Twisted Wave. 
This sometimes yields thousands of individual sounds. Being able to organize them is helpful when going through them and finding what you want. 

I thought re-ordering my sounds by something simple like basic RMS loudness would be simple. Couldn't find a solution so I wrote a simple script for it. 

## Getting this to run

I'm sure there are a lot of ways to do it. I setup the Jupyter notebook in VS Code then had to run a few shell commands to get everything up and running on a new machine:

Create a new environment

    python -m venv ./venv

Activate it
    source ./venv/bin/activate   

Install dependencies
    pip install -r ./requirements.txt 

Then, run the first block of code with the import statements. If that works, you're probably good. 

## Save a clean copy
Before you run the script, save a clean copy with no audio and you can use a duplicate when you want to run it. 

## Using it to organize samples
Inside the **audio_sort2** folder, load the audio files you want to sort in the **audio_files** folder. 

Run the 2nd block of code. This will take your original WAV files, copy them to the folder **output_by_max_rms**, then add the calculated max RMS value and rename the file with that at the front + your original filename. 

Then, when you import these sounds into the DAW from a file manager, they will be in order from quietest RMS level to loudest and you can decide where you're going to pull your sounds from. Usually the quieter samples are things like noise from handing the record, but these can sometimes be musically interesting too!


## other ways to organize sounds
There are also code blocks for ordering samples by length, summing RMS values, or average RMS. Length was kind of helpful, the other two not so much with the sounds I tested with. But I decided to just leave the code blocks in if you want to experiment. 

Simply uncomment them and they will run, then put the files in their respective folders. 

### File formats
Takes WAV files. 

