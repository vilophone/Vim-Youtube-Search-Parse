# Youtube Search Parser/Crawler/Scraper - Vim Script/Plugin
This plugin runs on any file that contains the html of a youtube search page. It finds the titles and links to the videos (from the YouTube search HTML) and deletes everything else in the file. You are left with a list of all the video titles and URLs from your search.

Setup:
1) put the .vim file in your /usr/share/vim/vimfiles/plugin directory
2) use vim YOUR_FILE -c ":call GetLinks()" in your terminal OR open YOUR_FILE in vim and type ":call GetLinks()" in normal mode

Example: 
1) $ curl https://www.youtube.com/results?search_query=rick+astley+never+gonna+give+you+up yt-search-html.txt
2) $ vim yt-search-html.txt -c ":call GetLinks()" -c ":normal ZZ"
3) $ cat yt-search-html.txt

Line 1: grabs the html from the search and puts it into a file (yt-search-html.txt)
Line 2: opens the file with the html in Vim, calls the plugin/function that finds the titles and URLs, then exits vim
Line 3: prints out all of the titles and URLs
