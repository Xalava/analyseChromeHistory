# Analyse your  google history

Original material https://applecrazy.github.io/blog/posts/analyzing-browser-hist-using-python/

Additional information: 


#Install dependencies

	pip3 install panda matplotlib

# Usage

	git clone 
	cd analyseChromeHistory
	# Retrive data ( see below for linux)
	python3 analyseHistory.py

# Retrieve your data on linux 

	mkdir data/
	cp .config/google-chrome/Default/History data/ChromeHistory
	sqlite3 ChromeHistory "select datetime(last_visit_time/1000000-11644473600,'unixepoch'),url from  urls order by last_visit_time desc" > data/hist.txt


