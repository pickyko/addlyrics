# addlyrics
Searches various websites and tags lyrics to local mp3 files.  Currently searches 5 websites:
* Musixmatch
* Genius
* Animelyrics
* Vocaloidlyrics
* Note

Work in progress.

## Requirements
Python, selenium with the geckodriver, eyed3, tqdm, and romkan (if using animelyrics.com).

## Usage
Edit `config.py` and point to your geckodriver and directory of mp3 files.  Enabling interactive mode in the config will make the program ask you if you want to search a website before searching, and will ask you if you want to write the lyrics found.  There is also the order in which websites will be searched.  You should edit it for your use case.

Some website scripts have whitelists for artists.  In the utils folder, edit where whitelist is assigned in the function.  The websites that currently have whitelists are note and vocaloid lyrics.  Artists not in the whitelist will not be searched for that website.  There are also blacklists.  If an artist is in the blacklist, it will not be searched on that website.  

The ignorelist.txt file is where you can put filenames of the mp3s you want the program to ignore.  The notfound.txt file is where the program will put names of the mp3s that lyrics could not be found for.  You can copy these filenames and put it in the ignorelist if you like.

After editing the config, run `main.py`.
