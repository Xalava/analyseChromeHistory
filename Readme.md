# Analyse your  google history

Analyse your 30 most frequented websites

Original material https://applecrazy.github.io/blog/posts/analyzing-browser-hist-using-python/

Additional information: 


## Install dependencies

	pip3 install panda matplotlib

## Usage

	git clone git@github.com:Xalava/analyseChromeHistory.git
	cd analyseChromeHistory
	# Retrieve data ( see below for linux)
	python3 analyseHistory.py

## Retrieve your data on linux 

	mkdir data/
	cp ~/.config/google-chrome/Default/History data/ChromeHistory
	sqlite3 data/ChromeHistory "select datetime(last_visit_time/1000000-11644473600,'unixepoch'),url from  urls order by last_visit_time desc" > data/hist.txt

NB: I had to remove the last entries as they had incoherent date